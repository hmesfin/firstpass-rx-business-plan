# FirstPass Rx — PA Citeria Extraction Worksheet Example

## Drug + PBM Combination Profile

---

| Field               | Value                  |
| ------------------- | ---------------------- |
| **Drug**            | Mounjaro (tirzepatide) |
| **PBM**             | Prime Therapeutics     |
| **Date Captured**   | January 2026           |
| **Captured By**     | [Pharmacist Name]      |
| **Last Verified**   | [Date]                 |
| **Next Review Due** | April 2026             |

---

## Section A: Drug Information

### Basic Identification

|Field|Value|
|---|---|
|Brand Name|Mounjaro|
|Generic Name|tirzepatide|
|Manufacturer|Eli Lilly and Company|
|Drug Class|GLP-1/GIP dual receptor agonist|
|Therapeutic Area|Diabetes / Weight Management|
|Route of Administration|Subcutaneous injection|
|Specialty Drug|Yes|

### Available Strengths

|Strength|NDC|Pen Configuration|
|---|---|---|
|2.5 mg/0.5 mL|00002-1452-80|4 single-dose pens per carton|
|5 mg/0.5 mL|00002-1453-80|4 single-dose pens per carton|
|7.5 mg/0.5 mL|00002-1454-80|4 single-dose pens per carton|
|10 mg/0.5 mL|00002-1455-80|4 single-dose pens per carton|
|12.5 mg/0.5 mL|00002-1456-80|4 single-dose pens per carton|
|15 mg/0.5 mL|00002-1457-80|4 single-dose pens per carton|

### Dosing Information

|Field|Value|
|---|---|
|Typical Starting Dose|2.5 mg once weekly|
|Titration Schedule|Increase by 2.5 mg every 4 weeks as tolerated|
|Maintenance Dose Range|5 mg to 15 mg once weekly|
|Maximum Dose|15 mg once weekly|

### FDA-Approved Indications

#### Indication 1: Type 2 Diabetes Mellitus

|Field|Value|
|---|---|
|Indication|Adjunct to diet and exercise to improve glycemic control in adults with type 2 diabetes mellitus|
|FDA Approval Date|May 13, 2022|

**Approved ICD-10 Codes:**

|Code|Description|Notes|
|---|---|---|
|E11.9|Type 2 diabetes mellitus without complications|Acceptable but less specific|
|E11.65|Type 2 diabetes mellitus with hyperglycemia|**Preferred** - demonstrates uncontrolled state|
|E11.8|Type 2 diabetes mellitus with unspecified complications|Acceptable|
|E11.69|Type 2 diabetes mellitus with other specified complication|Acceptable|
|E11.00-E11.59|Various T2DM with specific complications|All acceptable|

#### Indication 2: Chronic Weight Management

|Field|Value|
|---|---|
|Indication|Adjunct to reduced-calorie diet and increased physical activity for chronic weight management in adults with obesity (BMI ≥30) or overweight (BMI ≥27) with at least one weight-related comorbidity|
|FDA Approval Date|November 8, 2023 (as Zepbound, same molecule)|
|Note|Mounjaro is sometimes prescribed off-label for weight; Zepbound is the FDA-approved weight indication brand|

**Approved ICD-10 Codes for Weight Indication:**

|Code|Description|Notes|
|---|---|---|
|E66.01|Morbid (severe) obesity due to excess calories|**Preferred for BMI ≥40**|
|E66.09|Other obesity due to excess calories|For BMI 30-39.9|
|E66.1|Drug-induced obesity|If applicable|
|E66.9|Obesity, unspecified|Acceptable but less specific|
|Z68.35-Z68.45|BMI codes (35-45+)|Use as secondary code|

**Required Comorbidities if BMI 27-29.9:**

- Hypertension (I10)
- Type 2 diabetes (E11.*)
- Dyslipidemia (E78.*)
- Obstructive sleep apnea (G47.33)
- Cardiovascular disease (I25.*)

### Contraindications (Will Result in Denial)

|Contraindication|ICD-10|Notes|
|---|---|---|
|Type 1 diabetes|E10.*|Not FDA approved|
|Personal/family history of medullary thyroid carcinoma|C73, Z85.850, Z80.8|Black box warning|
|Multiple Endocrine Neoplasia syndrome type 2 (MEN 2)|E31.22|Black box warning|
|Known hypersensitivity to tirzepatide|T88.7||
|Pregnancy|Z33.*|Category X equivalent|

---

## Section B: PBM Submission Details

### Prime Therapeutics Profile

|Field|Value|
|---|---|
|PBM Name|Prime Therapeutics|
|PBM Code|PRIME|
|Parent Organization|Blue Cross Blue Shield Association (owned by 19 BCBS plans)|
|PA Phone|1-800-366-8343|
|PA Fax|1-877-357-4463|
|Provider Portal|https://www.myprime.com/provider|

### Submission Channels

|Channel|Availability|Details|
|---|---|---|
|**ePA (Electronic Prior Authorization)**|✅ Preferred|Via CoverMyMeds or Surescripts integration. Fastest response time.|
|**Provider Portal**|✅ Available|Log in at myprime.com. Requires registration. Can upload documents directly.|
|**Fax**|✅ Available|Use standard PA form. Include all supporting documentation.|
|**Phone**|⚠️ Limited|For urgent requests or status checks only. Cannot submit full PA by phone.|

### Response Time Expectations

|Request Type|Expected Response Time|
|---|---|
|Standard Request|48-72 hours|
|Urgent/Expedited|24 hours|
|ePA Submission|Often same-day for straightforward cases|

### Expedited Review Criteria

Expedited review is available when:

- Delay would seriously jeopardize life or health
- Delay would jeopardize ability to regain maximum function
- Patient is experiencing severe symptoms (e.g., DKA risk, severe hyperglycemia)

**How to request:** Check "Urgent" box on PA form and include clinical justification for urgency.

### Prime-Specific Quirks & Behaviors

|Category|Observation|
|---|---|
|Lab Recency|**Very strict** about 90-day lab recency. Will auto-reject if A1C is older than 90 days even if values are clearly documented.|
|Step Therapy Documentation|Requires **documented failure reason**, not just "patient tried metformin." Must specify why it failed (inadequate control, intolerance, contraindication).|
|Specialist Requirement|For weight management indication, may require prescription from or consultation with endocrinologist or obesity medicine specialist. Diabetes indication does not have this requirement.|
|Quantity Limits|Strict about 28-day supply. Will not approve 90-day fills even for stable patients.|
|Titration Enforcement|Monitors titration schedule. May question if patient jumps from 2.5mg directly to 10mg.|

---

## Section C: Required Clinical Data Fields

### Required Fields Summary

|Field|Required|Data Type|Validation Rules|
|---|---|---|---|
|Primary Diagnosis (ICD-10)|✅ Yes|ICD-10 code|Must be from approved list|
|Secondary Diagnosis|Conditional|ICD-10 code|Required if BMI 27-29.9 for weight indication|
|A1C Value|✅ Yes|Number|Must be ≥7.0 for diabetes indication|
|A1C Date|✅ Yes|Date|Must be within 90 days|
|BMI|Conditional|Number|Required for weight indication|
|Height|Conditional|Number (inches)|Required if submitting BMI|
|Weight|Conditional|Number (lbs)|Required if submitting BMI|
|Prior Medications|✅ Yes|List|Step therapy documentation|
|Prior Medication Dates|✅ Yes|Date ranges|Duration of each prior trial|
|Prior Medication Doses|✅ Yes|Text|Max dose achieved|
|Failure Reason per Med|✅ Yes|Text|Why each prior med was discontinued|
|Prescriber NPI|✅ Yes|10-digit NPI|Must be valid, active NPI|
|Prescriber Name|✅ Yes|Text|Must match NPI registry|
|Patient Member ID|✅ Yes|Text|From insurance card|
|Patient Date of Birth|✅ Yes|Date|For identity verification|
|Requested Dose|✅ Yes|Text|Starting dose or current dose|
|Quantity Requested|✅ Yes|Number|Typically 4 pens|
|Days Supply|✅ Yes|Number|Must be 28 days|

### Field-by-Field Details

#### Primary Diagnosis (ICD-10)

|Attribute|Value|
|---|---|
|Required|✅ Yes|
|Data Type|ICD-10 code|
|Validation|Must be from approved indication list|
|Common Mistakes|Using E11.9 (unspecified) when E11.65 (with hyperglycemia) is more appropriate and strengthens the case|
|Tip|**Always use the most specific code that accurately reflects the patient's condition**|

#### A1C Value

|Attribute|Value|
|---|---|
|Required|✅ Yes (for diabetes indication)|
|Data Type|Numeric (percentage)|
|Valid Range|5.0 - 20.0|
|Threshold for Approval|≥7.0% (demonstrates inadequate glycemic control)|
|Common Mistakes|Submitting without the lab report to back it up; transposing digits|
|Tip|If A1C is 6.8-6.9%, include additional evidence of poor control (glucose logs, symptoms)|

#### A1C Date

|Attribute|Value|
|---|---|
|Required|✅ Yes|
|Data Type|Date|
|Maximum Age|**90 days** (strictly enforced)|
|Common Mistakes|Submitting labs that are 91+ days old; not checking date before submission|
|Tip|**This is the #1 rejection reason.** Always verify lab date before submitting. If labs are 80+ days old, consider waiting for fresh labs or noting in submission that updated labs are pending.|

#### BMI

|Attribute|Value|
|---|---|
|Required|Conditional (required for weight management indication)|
|Data Type|Numeric|
|Threshold for Approval|≥30 OR ≥27 with documented comorbidity|
|Formula|Weight (lbs) × 703 ÷ Height (inches)²|
|Common Mistakes|Calculated BMI doesn't match height/weight provided; using outdated weight|
|Tip|Include height, weight, AND calculated BMI. Don't make the reviewer do math.|

#### Prior Medications Tried

|Attribute|Value|
|---|---|
|Required|✅ Yes (step therapy)|
|Data Type|Structured list|
|What to Include|Medication name, dose, dates, duration, reason for discontinuation|
|Common Mistakes|Just listing drug names without dates, doses, or failure reasons|
|Tip|**Be specific.** "Metformin 1000mg BID, 3/2024-9/2024, discontinued due to persistent GI intolerance despite dose adjustment" is far better than "Tried metformin - didn't tolerate"|

---

## Section D: Required Documents

### Document Checklist

|Document|Required|Recency Requirement|Must Include|
|---|---|---|---|
|Laboratory Results|✅ Yes|Within 90 days|A1C with date, basic metabolic panel|
|Prescriber Chart Notes|✅ Yes|Within 6 months|Diagnosis, treatment history, clinical rationale|
|Medication History|✅ Yes|N/A|Prior diabetes medications with dates, doses, outcomes|
|PA Form|Conditional|N/A|Required for fax submissions|
|Letter of Medical Necessity|Optional|N/A|Helpful for non-standard cases|
|Height/Weight Documentation|Conditional|Within 3 months|Required for weight indication|

### Document Details

#### Laboratory Results

**What must be included:**

- [ ] Hemoglobin A1C value
- [ ] A1C test date (must be within 90 days)
- [ ] Patient name and DOB on lab report
- [ ] Performing laboratory name
- [ ] Basic metabolic panel (recommended but not required)
- [ ] Lipid panel (recommended for comorbidity documentation)
- [ ] eGFR/creatinine (recommended for renal function documentation)

**Acceptable formats:** PDF, image (JPG/PNG), fax

**Tips:**

- Highlight or circle the A1C value and date
- If multiple pages, include only relevant pages
- Ensure patient name is visible on lab document
- If lab is close to 90-day limit, note the date prominently

#### Prescriber Chart Notes

**What must be included:**

- [ ] Date of recent office visit
- [ ] Documented diagnosis (T2DM and/or obesity)
- [ ] Current A1C or reference to recent labs
- [ ] List of current medications
- [ ] Documentation of prior diabetes medication trials
- [ ] Clinical rationale for Mounjaro specifically
- [ ] Treatment goals

**Tips:**

- A recent office visit note (within 6 months) is ideal
- If chart notes are lengthy, highlight relevant sections
- Include notes that document failed prior therapies

#### Medication History

**What must be included for each prior medication:**

|Element|Example|
|---|---|
|Medication name|Metformin ER|
|Maximum dose achieved|2000mg daily|
|Start date|January 2024|
|End date (or "ongoing")|June 2024|
|Duration|6 months|
|Outcome/Reason for change|A1C remained 8.2% despite maximum tolerated dose|

**Acceptable sources:**

- Pharmacy records
- Chart notes documenting medication history
- Patient's medication list from EHR

---

## Section E: Step Therapy Requirements

### Step Therapy Overview

|Field|Value|
|---|---|
|Step Therapy Required|✅ Yes|
|Number of Steps|2 steps before Mounjaro|
|Exception Process|Available for documented contraindications or previous trials|

### Step Therapy Details

#### Step 1: Metformin Trial

|Requirement|Details|
|---|---|
|Required Medication|Metformin (any formulation)|
|Acceptable Brands|Glucophage, Glucophage XR, Glumetza, Fortamet, Riomet, generic metformin|
|Minimum Duration|**3 months** (12 weeks)|
|Minimum Dose|**1500mg daily** (preferred: max tolerated dose up to 2000mg)|
|Target|A1C reduction or documented intolerance|

**What counts as "failure" for Step 1:**

|Failure Type|Documentation Required|
|---|---|
|Inadequate efficacy|A1C remains ≥7.0% after ≥3 months at max tolerated dose|
|Intolerance|Documented GI side effects (nausea, diarrhea, abdominal pain) despite dose adjustment|
|Contraindication|eGFR <30, documented lactic acidosis risk, severe hepatic impairment|
|Allergy|Documented allergic reaction|

**Documentation must include:**

- Specific dates of metformin use
- Maximum dose achieved
- Duration at maximum dose
- A1C values before and after trial (if efficacy failure)
- Specific symptoms experienced (if intolerance)
- Lab values demonstrating contraindication (if applicable)

#### Step 2: Second-Line Agent Trial

|Requirement|Details|
|---|---|
|Required|Trial of at least ONE second-line agent|
|Minimum Duration|**3 months**|

**Acceptable second-line agents:**

|Drug Class|Examples|Notes|
|---|---|---|
|Sulfonylureas|glipizide, glimepiride, glyburide|Common, inexpensive|
|SGLT2 Inhibitors|Jardiance (empagliflozin), Farxiga (dapagliflozin), Invokana (canagliflozin)|**Preferred by Prime** due to CV/renal benefits|
|DPP-4 Inhibitors|Januvia (sitagliptin), Tradjenta (linagliptin), Onglyza (saxagliptin)|Well-tolerated option|
|Thiazolidinediones|Actos (pioglitazone)|Less commonly used|

**What counts as "failure" for Step 2:**

|Failure Type|Documentation Required|
|---|---|
|Inadequate efficacy|A1C remains ≥7.0% after ≥3 months at therapeutic dose|
|Intolerance|Documented side effects specific to drug class|
|Contraindication|Class-specific contraindications documented|

**Pro tip:** SGLT2 inhibitors are Prime's preferred second-line class. If patient tried an SGLT2 and it didn't work, this strengthens the case significantly.

### Step Therapy Exceptions

|Exception Type|Criteria|Documentation Required|
|---|---|---|
|Contraindication to metformin|eGFR <30, history of lactic acidosis, severe hepatic impairment|Lab results, chart notes|
|Contraindication to all second-line agents|Multiple documented contraindications|Detailed clinical notes|
|Previous adequate trial|Patient previously completed step therapy at another plan|Prior pharmacy records, chart notes, previous PA approval|
|Urgent clinical need|DKA risk, A1C >10%, severe symptoms|Clinical documentation, lab results|

**How to document exceptions:**

1. Clearly state which step is being excepted
2. Provide specific clinical rationale
3. Include supporting documentation (labs, chart notes)
4. Use language: "Patient meets exception criteria for [Step X] due to [specific reason]"

### Step Therapy Insider Tips

> **TIP 1:** Document WHY each medication failed, not just that it was tried. "Metformin discontinued due to intolerance" will be rejected. "Metformin 1500mg discontinued after 4 months due to persistent diarrhea (3-4 episodes daily) despite gradual titration and trial of extended-release formulation" will be approved.

> **TIP 2:** If a patient has a true contraindication to metformin, LEAD with that. It's an easy exception and skips Step 1 entirely. Don't bury it in the notes.

> **TIP 3:** Prime is more lenient on Step 2 than Step 1. If metformin trial is well-documented, the second-line requirement is sometimes approved with less documentation.

> **TIP 4:** If patient has been on a stable GLP-1 (like Ozempic or Trulicity) and is switching to Mounjaro, prior GLP-1 use often satisfies the step therapy requirement. Document the prior GLP-1, dose, duration, and reason for switch.

---

## Section F: Lab Requirements

### Required Labs

|Lab Test|Required|LOINC Code|Max Age|Threshold|Notes|
|---|---|---|---|---|---|
|Hemoglobin A1C|✅ Yes|4548-4|**90 days**|≥7.0% for approval|**Strictly enforced**|
|eGFR|Recommended|33914-3|90 days|≥15 for safety|Required if patient >65 or has CKD history|
|Serum Creatinine|Recommended|2160-0|90 days|N/A|Used to calculate eGFR|
|Fasting Glucose|Optional|1558-6|90 days|N/A|Supports diagnosis if A1C borderline|
|Lipid Panel|Optional|57698-3|12 months|N/A|Helpful for comorbidity documentation|

### Lab Thresholds and Logic

#### A1C Decision Logic

```
IF A1C ≥ 7.0% AND within 90 days:
    → Meets glycemic control criteria
    
IF A1C 6.5% - 6.9% AND within 90 days:
    → May require additional justification
    → Include: glucose logs, symptoms, complication risk factors
    
IF A1C < 6.5%:
    → Will likely be denied for diabetes indication
    → Consider: Is patient on current therapy that's working? Document why switch is needed.
    
IF A1C > 90 days old:
    → AUTO-REJECT regardless of value
    → Must obtain updated labs before submission
```

#### Lab Documentation Tips

> **TIP 1:** Even if only A1C is "required," including a full metabolic panel (BMP) shows thoroughness and prevents follow-up requests.

> **TIP 2:** If A1C is borderline (7.0-7.2%), include glucose logs or CGM data showing variability/poor control that A1C doesn't capture.

> **TIP 3:** If patient has CKD, ALWAYS include eGFR. Prime will check for renal contraindications.

> **TIP 4:** Ensure the lab report clearly shows the **date of collection**, not just the date of report. Prime uses collection date for the 90-day calculation.

---

## Section G: Quantity/Dosing Limits

### Standard Quantity Limits

|Strength|Quantity per Fill|Days Supply|Refill Frequency|
|---|---|---|---|
|2.5 mg|4 pens|28 days|Every 28 days|
|5 mg|4 pens|28 days|Every 28 days|
|7.5 mg|4 pens|28 days|Every 28 days|
|10 mg|4 pens|28 days|Every 28 days|
|12.5 mg|4 pens|28 days|Every 28 days|
|15 mg|4 pens|28 days|Every 28 days|

### Quantity Limit Notes

|Rule|Details|
|---|---|
|Max days supply|28 days (no 90-day fills)|
|Vacation override|Available with advance request (up to 84-day supply)|
|Early refill|Allowed at 75% of days supply (day 21+)|
|Titration monitoring|Prime tracks titration; rapid escalation may trigger review|

### Titration Schedule Expectations

|Week|Expected Dose|Notes|
|---|---|---|
|Weeks 1-4|2.5 mg|Initiation dose|
|Weeks 5-8|5 mg|First maintenance dose|
|Weeks 9-12|7.5 mg|If needed|
|Weeks 13-16|10 mg|If needed|
|Weeks 17-20|12.5 mg|If needed|
|Weeks 21+|15 mg|Maximum dose|

> **TIP:** If prescriber wants to start at a higher dose (e.g., patient switching from high-dose Ozempic), document the rationale. Don't just submit for 10mg on a new PA without explanation.

---

## Section H: Common Rejection Reasons

### Rejection Frequency Analysis

|Rank|Rejection Reason|Frequency|Impact|
|---|---|---|---|
|1|Labs older than 90 days|**Very Common** (35% of rejections)|Auto-reject|
|2|Incomplete step therapy documentation|**Very Common** (30% of rejections)|Additional info request|
|3|Missing failure reason for prior meds|**Common** (15% of rejections)|Additional info request|
|4|Diagnosis code not supported|**Occasional** (10% of rejections)|Denial|
|5|Missing prescriber NPI or mismatch|**Occasional** (5% of rejections)|Processing delay|
|6|Quantity/days supply mismatch|**Rare** (3% of rejections)|Easy fix|
|7|Duplicate PA on file|**Rare** (2% of rejections)|Processing delay|

### Detailed Rejection Analysis

#### Rejection #1: Labs Older Than 90 Days

|Field|Details|
|---|---|
|Frequency|**Very Common** - #1 cause of rejection|
|Error Message|"Laboratory results exceed 90-day recency requirement"|
|How to Avoid|Always verify A1C date before submission. If labs are 75+ days old, consider waiting for updated labs.|
|If Rejected|Obtain new labs and resubmit. Cannot appeal without updated labs.|

#### Rejection #2: Incomplete Step Therapy Documentation

|Field|Details|
|---|---|
|Frequency|**Very Common**|
|Error Message|"Insufficient documentation of required prior therapies"|
|How to Avoid|Include specific dates, doses, duration, and outcome for EACH prior medication|
|If Rejected|Submit additional documentation. Often approved on resubmission with complete info.|

**Example of INSUFFICIENT documentation:**

> "Patient tried metformin and Januvia without success."

**Example of SUFFICIENT documentation:**

> "Metformin ER: 500mg daily initiated 1/15/2024, titrated to 2000mg daily by 3/1/2024. A1C on 4/15/2024 was 8.1% (down from 8.9%). Discontinued 6/1/2024 due to persistent GI intolerance (daily diarrhea) despite extended-release formulation.
> 
> Januvia: 100mg daily initiated 6/15/2024. A1C on 9/20/2024 was 7.9%. Inadequate response despite 3+ months of therapy. Current A1C 12/15/2024 is 7.8%."

#### Rejection #3: Missing Failure Reason for Prior Meds

|Field|Details|
|---|---|
|Frequency|**Common**|
|Error Message|"Documentation does not indicate reason for discontinuation of prior therapy"|
|How to Avoid|For EACH prior medication, state: efficacy failure (with A1C values) OR intolerance (with specific symptoms) OR contraindication (with clinical basis)|
|If Rejected|Add specific failure documentation and resubmit|

#### Rejection #4: Diagnosis Code Not Supported

|Field|Details|
|---|---|
|Frequency|**Occasional**|
|Error Message|"Diagnosis code not approved for requested medication"|
|How to Avoid|Use ICD-10 codes from the approved list. Avoid E10.* (Type 1) codes.|
|If Rejected|Verify diagnosis. If T2DM, correct the code and resubmit. If T1DM, PA will not be approved.|

---

## Section I: Insider Tips

### Documentation Tips

|Tip|Importance|Details|
|---|---|---|
|Lead with the strongest evidence|🔴 High|If A1C is 9.5%, put that front and center. If patient failed 3 prior meds, summarize that upfront.|
|Include labs even if "attached separately"|🔴 High|Don't just reference attachments. Put key values (A1C, date) in the form fields AND attach the lab report.|
|Use clinical language|🟡 Medium|"Failed to achieve glycemic target" > "Didn't work well"|
|Date everything|🔴 High|Every medication trial, every lab, every office visit should have specific dates.|

### Language That Works

**For step therapy:**

> ✅ "Patient completed adequate trial of metformin 2000mg daily for 4 months (January-May 2024) with documented inadequate response (A1C 8.2% on 5/15/2024, down from 8.9% at initiation). Metformin discontinued and Jardiance 25mg initiated June 2024. After 3 months on Jardiance (A1C 7.8% on 9/20/2024), patient has not achieved glycemic target of <7.0%. Mounjaro requested for additional A1C reduction."

**For clinical necessity:**

> ✅ "Patient's current A1C of 8.1% on maximally tolerated oral therapy places them at significantly elevated risk for microvascular complications. Addition of tirzepatide is clinically indicated to achieve glycemic target and reduce complication risk."

**For GI intolerance:**

> ✅ "Metformin discontinued due to intractable gastrointestinal adverse effects (persistent diarrhea 4-5 episodes daily, nausea, abdominal cramping) despite trial of extended-release formulation and gradual dose titration over 8 weeks."

### Timing Tips

|Tip|Details|
|---|---|
|Submit early in the week|Monday-Wednesday submissions typically get faster turnaround. Friday submissions may sit until Monday.|
|Avoid month-end|PBM volume is higher at month-end. Mid-month submissions often process faster.|
|Morning submissions|ePA submissions before noon (Central Time) are more likely to be processed same-day.|
|Plan for titration|Submit PA 1-2 weeks before patient runs out of current strength to allow time for titration dose approval.|

### Relationship Tips

|Scenario|Approach|
|---|---|
|Status check|Call PA line after 48 hours if no response. Reference case number.|
|Missing info request|Respond within 24 hours if possible. Faster response = faster approval.|
|Denial received|Always request peer-to-peer before formal appeal. P2P overturn rate is ~60% at Prime.|
|Complex case|Consider proactive peer-to-peer before submission for unusual cases.|

### What Reviewers Actually Look At First

Based on pharmacist experience, Prime reviewers typically scan in this order:

1. **A1C value and date** — Is it recent enough? Is it high enough?
2. **Diagnosis code** — Is it an approved indication?
3. **Step therapy summary** — Did they try metformin? Second-line agent?
4. **Documentation completeness** — Are labs attached? Chart notes?
5. **Prescriber credentials** — Valid NPI? Appropriate specialty?

> **Key insight:** Make the first four items immediately visible and clearly documented. Don't make the reviewer hunt for information.

---

## Section J: Appeal Strategies

### Denial Response Decision Tree

```
DENIAL RECEIVED
      │
      ▼
┌─────────────────────────────────────┐
│ Is it a "Missing Information" denial?│
└─────────────────────────────────────┘
      │
      ├── YES → Gather missing info and RESUBMIT (not appeal)
      │
      └── NO → Continue below
              │
              ▼
┌─────────────────────────────────────┐
│ Is the denial clinically defensible?│
│ (i.e., do you have a strong case?) │
└─────────────────────────────────────┘
      │
      ├── YES → Request PEER-TO-PEER first
      │         (60%+ overturn rate at Prime)
      │
      └── NO → Consider alternative medication
              or address underlying issue
```

### Peer-to-Peer Review

#### When to Request P2P

- Denial reason is "not medically necessary" but you have clear clinical rationale
- Denial reason is "step therapy not met" but patient has valid exception
- Denial reason seems to misunderstand the clinical situation

#### P2P Preparation Checklist

- [ ] Have prescribing physician available for the call
- [ ] Prepare a 2-minute verbal summary of the case
- [ ] Have all relevant labs, dates, and prior medication history in front of you
- [ ] Know the specific denial reason and be prepared to address it
- [ ] Have supporting literature/guidelines ready if applicable (e.g., ADA Standards of Care)

#### P2P Success Tips

|Tip|Details|
|---|---|
|Be concise|Reviewers do many P2P calls. Get to the point in first 2 minutes.|
|Address denial reason directly|Don't rehash entire history. Focus on why the denial reason doesn't apply.|
|Cite guidelines|Reference ADA Standards of Care, AACE guidelines if applicable.|
|Emphasize patient-specific factors|Why does THIS patient need Mounjaro specifically?|
|Stay professional|Even if frustrating, maintain collegial tone.|

### Appeal by Denial Reason

#### Denial: "Step Therapy Requirement Not Met"

|Strategy|Details|
|---|---|
|First action|Request P2P|
|Documentation to add|Complete medication history with specific dates, doses, duration, failure reasons|
|Key argument|Either: (1) Step therapy WAS completed - here's the documentation, OR (2) Patient qualifies for exception due to [contraindication/prior trial/urgent need]|
|Success rate|High if documentation supports the case|

#### Denial: "Not Medically Necessary"

|Strategy|Details|
|---|---|
|First action|Request P2P|
|Documentation to add|Letter of medical necessity from prescriber, ADA guidelines citation, patient-specific risk factors|
|Key argument|Current therapy is inadequate; patient is at elevated complication risk; Mounjaro's dual mechanism offers unique benefit|
|Success rate|Moderate - depends on strength of clinical case|

#### Denial: "Diagnosis Not Covered"

|Strategy|Details|
|---|---|
|First action|Verify diagnosis coding is accurate|
|If coding error|Resubmit with correct ICD-10 code|
|If diagnosis truly not covered|This is a harder appeal. May need exception process or alternative medication.|
|Success rate|Low unless it was a coding error|

---

## Section K: Source Documentation

### Official Prime Resources

|Document|URL|Last Accessed|
|---|---|---|
|Prime Therapeutics Provider Portal|https://www.myprime.com/provider|[Date]|
|Mounjaro PA Criteria (Prime)|[Insert URL when obtained]|[Date]|
|Prime PA Forms|https://www.primetherapeutics.com/pa-forms|[Date]|

### Clinical Guidelines

|Guideline|Organization|URL|
|---|---|---|
|Standards of Medical Care in Diabetes|American Diabetes Association|https://diabetesjournals.org/care|
|Obesity Management Guidelines|American Association of Clinical Endocrinology|https://www.aace.com|
|Mounjaro Prescribing Information|Eli Lilly|https://uspl.lilly.com/mounjaro/mounjaro.html|

### Verification Schedule

|Item|Frequency|Next Due|
|---|---|---|
|PA criteria verification|Quarterly|April 2026|
|Formulary status check|Quarterly|April 2026|
|Quantity limit verification|Annually|January 2027|
|Step therapy requirements|Quarterly|April 2026|

---

## Section L: Quick Reference Card

### Mounjaro + Prime: At-a-Glance Checklist

**Before You Submit:**

- [ ] A1C value ≥7.0%
- [ ] A1C date within 90 days (CHECK THE DATE!)
- [ ] Diagnosis code from approved list (E11.65 preferred for T2DM)
- [ ] Step 1 documented: Metformin trial (3+ months, 1500mg+, with failure reason)
- [ ] Step 2 documented: Second-line agent trial (3+ months, with failure reason)
- [ ] Lab report attached
- [ ] Chart notes attached
- [ ] Prescriber NPI verified
- [ ] Quantity = 4 pens, Days supply = 28

**Red Flags That Will Cause Rejection:**

- ❌ A1C older than 90 days
- ❌ A1C < 7.0% without additional justification
- ❌ Step therapy listed without dates, doses, or failure reasons
- ❌ Type 1 diabetes diagnosis (E10.*)
- ❌ Missing lab documentation
- ❌ Quantity/days supply mismatch

**If Denied:**

1. Check denial reason carefully
2. If missing info → resubmit with additional documentation
3. If clinical denial → request peer-to-peer FIRST
4. Have prescriber available for P2P call
5. 60%+ of Prime denials are overturned at P2P

---

## Revision History

|Date|Version|Changes|Author|
|---|---|---|---|
|January 2026|1.0|Initial document creation|[Name]|
|||||

---

_This document is proprietary to FirstPass Rx and contains confidential operational information. Do not distribute externally._