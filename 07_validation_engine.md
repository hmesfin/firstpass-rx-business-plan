This is a non-technical walkthrough of how FirstPass Rx decides whether a prior
authorization (PA) request is likely to be approved. Read this before diving
into the code in `backend/apps/formulary/validators/`.

## The Big Picture

When a clinic submits a PA request, we want to answer one question:

> Based on what the PBM requires, does this submission have everything it
> needs to get approved?

We answer that by running the submission through a set of **rules**. Each rule
checks one specific thing ("is there a qualifying diagnosis?", "did the patient
try the required step-therapy drugs first?", "is the A1C lab recent enough?").
A **validator** is just a bundle of rules for a particular drug class and
program type.

Think of it like a checklist at the DMV: the validator is the checklist, each
rule is one line on the checklist, and the submission either checks the box or
doesn't.

## The Three Moving Parts

### 1. The Submission Context

This is the "patient folder" we hand to the rules. It contains everything a
rule might need to make a decision: the patient's diagnosis, age, labs, which
drug is being requested, which drugs they've tried before, any allergies or
contraindications, the prescriber's notes, and the PBM's criteria document for
this drug.

The important thing: the rules never go looking for this information
themselves. They just read what's in the folder. If the folder is missing
something, the rule fails cleanly — it doesn't crash trying to find it.

### 2. A Rule

A rule is the smallest unit of checking. One rule = one question. Examples:

- *"Does the patient have a diagnosis code that matches what the PBM requires
  for this drug?"*
- *"Is the patient's A1C recent enough and high enough to qualify for a GLP-1?"*
- *"Has the patient tried at least two preferred drugs before this one?"*
- *"Is the patient old enough for this medication?"*

Every rule returns three things: did it pass, what's the human-readable
message, and is the rule required (a required failure blocks the PA; an
optional failure just means a reviewer needs to take a look).

Rules are deliberately tiny. One rule, one question. This is what keeps the
system easy to reason about and easy to test — and it's what will let us slot
in LLM-powered rules later without rewriting anything.

### 3. A Validator

A validator is a named bundle of rules for a specific drug class and program
type. For example:

- `GLP1PriorAuthValidator` — the PA checklist for GLP-1s (Ozempic,
  Wegovy, Mounjaro, etc.)
- `GLP1StepTherapyValidator` — the step therapy checklist for GLP-1s
- `QuantityLimitValidator` — the "is the requested quantity within the PBM's
  limit?" checklist

A validator's only job is to say "these are my rules" and then run them all
against the submission context. It then rolls up the individual rule results
into one overall answer:

- **Approved** — every required rule passed.
- **Needs review** — every required rule passed, but at least one optional
  rule flagged something a human should eyeball.
- **Denied** — at least one required rule failed; the PA is very unlikely to
  be approved as-is.

That's it. No scoring, no AI, no magic — just a checklist walked in order.

## How It Gets Used

For each submission we need to validate, someone has to decide *which*
validator(s) apply. Today that decision is made by reading the
`CriteriaSet.validator_class` field on the PBM's criteria record — it
literally names the validator class to use ("use `GLP1PriorAuthValidator` for
this drug+PBM combination").

Once we know which validator to run, we:

1. Build the submission context (gather the patient folder).
2. Hand it to the validator.
3. The validator runs its rules in order.
4. We get back an overall result plus a list of per-rule outcomes and a list
   of denial reasons.

That result is what the reviewer sees in the workbench, and it's what the API
returns to the frontend.

## What We're Building on Top of This

The existing framework handles the deterministic parts well — checklists that
can be answered with a yes/no from structured data. The validation engine
we're about to build adds four things *around* it:

1. **Generic validators** for the five common checklist dimensions every drug
   shares: required fields, required documents, required labs, step therapy,
   and diagnosis. Today we have drug-class-specific validators (GLP-1s,
   quantity limits); we're adding the generic ones that apply everywhere.
2. **A criteria adapter** — a translator that reads the structured PBM
   criteria from the ingestion pipeline and hands the rules the exact shapes
   they need ("give me the required labs for this drug", "give me the
   required ICD-10 codes"). Rules never have to know how the criteria are
   stored.
3. **A scoring layer** — a separate pass that converts a validator's yes/no
   rule results into a 0-100 score. Kept separate so the clinical team can
   tune the scoring weights without anyone touching the rules.
4. **A recommendation layer** — takes the validator result plus the score and
   produces a plain-English "do this next" message for the reviewer.

And one thing the engine will *not* do: we are not building "drug-specific
validators" in this milestone (like `SemaglutideValidator`). The existing
GLP-1 and quantity-limit validators stay. The registry we're adding will
support registering new drug-class validators later as one-file changes.

## Where AI Fits In (Later)

The framework was designed so that LLM-powered validation can be added
without rewriting anything. There are three sensible places to plug in an
LLM:

### As a single rule

The most natural fit. Because a rule is just "given this context, return
pass/fail and a message", an LLM can be wrapped in a single rule. Example:
`LLMClinicalNarrativeRule` reads the prescriber's free-text statements from
the submission context and asks the LLM "based on these notes, does the
patient meet the PBM's clinical criteria for this drug?" The rule returns
pass/fail just like any other rule. The validator doesn't know or care that
one of its rules happens to call an LLM.

This is the cleanest path and it's the one we'll reach for first when the
Clinical Lead identifies a criterion that can't be answered with structured
data alone.

### As a pre-processing step

Before the validator ever runs, we need to build the submission context. If
a clinic uploads scanned lab results or a free-text clinical note, we need
to extract structured values from them (A1C, weight, diagnosis date) to
populate the context. That extraction job is a natural fit for an LLM, and
it's entirely separate from validation — the validator still sees a clean,
structured context and stays deterministic.

This is already the pattern the criteria ingestion pipeline uses on the PBM
side (PDFs → LLM → structured criteria). The same pattern applies to
patient documents.

### As a post-processing "second opinion"

After the rules run and the scoring layer produces a score, we can
optionally hand the full result + the raw criteria to an LLM and ask it
"anything the rules missed? What should the reviewer do next?" This
produces richer remediation advice than a rule-based recommendation
service, and it runs at the very end, where latency and nondeterminism are
tolerable.

### Why not put the LLM in the engine itself?

The validation engine's job is to dispatch to validators and aggregate
results. That's it. Keeping the engine dumb means:

- Deterministic rules are fast and cheap — most validations don't need an
  LLM at all.
- LLM calls are isolated to specific rules or to the pre/post layers,
  where they're easy to mock in tests and easy to turn off.
- The clinical team can see exactly which rules are LLM-powered and which
  aren't — important for audit and compliance.

If the engine itself called the LLM, every validation would pay that cost,
the seams for testing would disappear, and we'd lose the ability to reason
about which parts of the decision are deterministic versus probabilistic.

## The One-Paragraph Summary

We have a checklist framework. Each checklist is a **validator**. Each line
on the checklist is a **rule**. The **submission context** is the patient
folder we hand to the checklist. The result is **approved**, **needs review**,
or **denied** with a list of reasons. We're adding generic checklists for
common PBM requirements, a translator that feeds the checklists from our
criteria database, and separate scoring and recommendation layers on top.
AI rules can be added later as just another kind of checklist line.
