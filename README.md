# FirstPass Rx — Business Planning Documents

## Project Summary

**FirstPass Rx** is a specialty drug prior authorization validation service designed to maximize first-pass approval rates through PBM-specific pre-submission validation.

### The Problem

- Prior authorizations for specialty drugs fail 30-40% of the time
- Not because patients don't qualify, but because submissions are incomplete
- Outdated labs, missing documentation, and insufficient step therapy evidence cause delays
- Each rejection means 2+ weeks of delayed treatment and $200+ in administrative rework

### The Solution

FirstPass Rx validates PA submissions against PBM-specific criteria before they're submitted:

- **Validate completeness** — Check every required field, document, and data point
- **Apply PBM-specific rules** — Know what each PBM actually needs
- **Flag gaps before submission** — Catch issues before the PBM rejects them
- **Expert review** — Trained specialists QA every submission

**Target: 85%+ first-pass approval rate** (vs. industry average of 60-65%)

### Market Opportunity

| Metric | Value |
|--------|-------|
| US Specialty Drug Spend | $350B+ annually |
| Specialty Drugs Requiring PA | >90% |
| Target Segments | Oncology, Dermatology, Endocrinology, Rheumatology |

### Team

| Role | Person | Background |
|------|--------|------------|
| Co-Founder & CEO | Hamel Mesfin | Former VP at Prime Therapeutics, 20+ years healthcare insurance |
| Co-Founder & CCO | Yonatan Berhe | Pharmacist with PBM/specialty pharmacy PA experience |
| Clinical Advisor | TBD | Practicing specialist (oncology, derm, or endo) |

### Timeline

| Milestone | Date |
|-----------|------|
| Knowledge extraction complete | January 2026 |
| MVP platform ready | February 2026 |
| Pilot customers signed | March 2026 |
| **Live pilot launch** | **April 1, 2026** |
| Pilot results & case studies | June 2026 |

---

## Table of Contents

### [00. Executive Summary](./00_executive_summary.md)

**One-page overview of FirstPass Rx business concept**

- Problem statement: PA failures due to incomplete submissions
- Solution overview: Pre-submission validation with PBM-specific knowledge
- Market opportunity: $350B specialty drug market
- Team qualifications
- Business model: Per-submission + success fee ($75-100/PA)
- Go-to-market timeline

**Best for:** Quick overview, stakeholder introductions, pitch summary

---

### [01. Stakeholder Presentation](./01_steakholder_presentation.md)

**Comprehensive slide-deck style presentation for potential partners, advisors, and investors**

- The Problem: Data on PA failures and impact
- The Solution: How FirstPass Rx works
- The Market: Specialty drug growth and target segments
- Competitive Landscape: Gaps in current solutions
- Business Model: Unit economics and customer ROI
- Go-to-Market Plan: Pilot → Growth → Scale
- Team Backgrounds: Why this team is uniquely qualified
- Investment & Resources: Bootstrap to seed approach
- Risk & Mitigation: Key risks and how to address them
- The Ask: What FirstPass Rx needs from stakeholders

**Best for:** Formal presentations, investor meetings, partner discussions

---

### [02. Project Plan](./02_project_plan.md)

**Detailed execution plan for April 1, 2026 pilot launch**

#### Phase 1: Foundation (January 2026)

- Business formation & legal (LLC, operating agreement, BAAs)
- Knowledge extraction (15-20 drug/PBM combinations documented)
- Infrastructure setup (server, database, CI/CD)
- Team alignment (equity, roles, commitments)

#### Phase 2: Build (February 2026)

- Backend development (Django/DRF API)
- Validation engine (PBM-specific rules, drug-specific logic)
- Frontend development (Vue.js reviewer workbench)
- Data seeding (populate database with extracted criteria)

#### Phase 3: Test & Recruit (March 2026)

- System testing with realistic scenarios
- Pilot customer acquisition (sign 2-3 practices)
- Operational preparation (processes, guides, procedures)
- Training (reviewer training curriculum)

#### Phase 4: Launch Prep (Late March 2026)

- Go-live readiness verification
- Customer onboarding

**Includes:** Task lists, deliverables, milestones, risk register, communication plan

**Best for:** Project execution tracking, task management, milestone planning

---

### [03. Criteria Extraction Worksheet (Example)](./03_criteria_extraction_worksheet.md)

**Fully completed example: Mounjaro + Prime Therapeutics PA criteria**

Demonstrates the depth of PBM knowledge captured:

- Section A: Drug Information (indications, ICD-10 codes, contraindications)
- Section B: PBM Submission Details (channels, response times, quirks)
- Section C: Required Clinical Data Fields (validation rules, thresholds)
- Section D: Required Documents (what must be included)
- Section E: Step Therapy Requirements (metformin, second-line agents)
- Section F: Lab Requirements (A1C thresholds, 90-day recency rules)
- Section G: Quantity/Dosing Limits
- Section H: Common Rejection Reasons (with examples)
- Section I: Insider Tips (language that works, timing, reviewer priorities)
- Section J: Appeal Strategies (peer-to-peer process)
- Section K: Source Documentation
- Section L: Quick Reference Card

**Key insight example:** Prime Therapeutics is **very strict** about 90-day lab recency — they auto-reject A1C older than 90 days even if values are clearly documented.

**Best for:** Understanding the depth of knowledge captured, training new reviewers, seeing what "insider knowledge" means

---

### [04. Criteria Extraction Worksheet (Blank Template)](./04_blank_extraction_worksheet.md)

**Empty template for knowledge extraction sessions with pharmacist partner**

Use this template to document PA criteria for each Drug + PBM combination:

- Structured sections matching the example (A-L)
- Checklists for required data points
- Tables for validation rules, thresholds, and PBM quirks
- Space for insider tips and appeal strategies
- Revision history tracking

**How to use:** Complete one worksheet per Drug + PBM combination during knowledge extraction sessions with pharmacist partner.

**Best for:** Knowledge capture, maintaining criteria library, onboarding new team members

---

### [05. Partners & Advisors Agreement]((./05_partners_and_advisors.md)

**Discussion guide for structuring co-founder and advisor relationships**

#### Part 1: Co-Founder/Partner Agreement

For the pharmacist partner (clinical lead):

- Ownership & Equity (splits, vesting schedules)
- Roles & Responsibilities (time commitments, decision authority)
- Compensation (salary vs. equity vs. revenue share)
- Capital Contributions (who funds what)
- Decision-Making & Governance (deadlock resolution)
- Intellectual Property (assignment, pre-existing IP)
- Confidentiality, Non-Compete, Non-Solicit
- Departure & Exit Provisions (buyback rights, valuation)
- Sale of the Company (drag-along, tag-along rights)
- Dispute Resolution (mediation, arbitration)

**Sample term sheet included**

#### Part 2: Advisor Agreement

For the physician advisor:

- Advisor responsibilities (time commitment: 2-4 hours/month)
- Compensation (0.25% - 0.5% equity, 2-year vesting)
- Term and termination
- Confidentiality and conflicts
- Sample advisor term sheet

#### Part 3: Discussion Questions

Key questions to ask pharmacist partner and physician advisor to ensure alignment.

**Disclaimer:** This document is a discussion outline only, not legal advice. Consult an attorney before finalizing agreements.

**Best for:** Partner discussions, aligning expectations, preparing for attorney engagement

---

## How to Use These Documents

### For the Founding Team

1. **Start with [00. Executive Summary](./00_executive_summary.md)** — Ensure alignment on the core concept
2. **Review [02. Project Plan](./02_project_plan.md)** — Assign tasks and set up weekly syncs
3. **Use [04. Blank Template](./04_blank_extraction_worksheet.md)** — Begin knowledge extraction sessions immediately
4. **Work through [05. Partners & Advisors](./05_partners_and_advisors.md)** — Document equity, roles, and expectations

### For Potential Partners or Advisors

1. **Read [00. Executive Summary](./00_executive_summary.md)** — 5-minute overview
2. **Review [01. Stakeholder Presentation](./01_steakholder_presentation.md)** — Full context on opportunity, team, and ask
3. **Skim [03. Example Extraction](./03_criteria_extraction_worksheet.md)** — See what "insider knowledge" looks like
4. **Discuss [05. Partners & Advisors](./05_partners_and_advisors.md)** — Understand relationship structure

### For Pilot Customers

1. **Read [00. Executive Summary](./00_executive_summary.md)** — Understand the value proposition
2. **Review the "Example ROI" section in [01. Stakeholder Presentation](./01_steakholder_presentation.md)** — See potential savings
3. **Ask to see [03. Example Extraction](./03_criteria_extraction_worksheet.md)** — Understand depth of expertise

### For Investors (if external capital sought)

1. **Read [01. Stakeholder Presentation](./01_steakholder_presentation.md)** — Full investment case
2. **Review [02. Project Plan](./02_project_plan.md)** — Execution capability
3. **Check [05. Partners & Advisors](./05_partners_and_advisors.md)** — Team structure and commitments

---

## Document Status

| Document | Version | Last Updated | Status |
|----------|---------|--------------|--------|
| Executive Summary | 1.0 | January 2026 | ✅ Complete |
| Stakeholder Presentation | 1.0 | January 2026 | ✅ Complete |
| Project Plan | 1.0 | January 2026 | ✅ Complete |
| Criteria Extraction (Example) | 1.0 | January 2026 | ✅ Complete |
| Criteria Extraction (Template) | 1.0 | January 2026 | ✅ Complete |
| Partners & Advisors | 1.0 | January 2026 | ✅ Complete |

---

## Key Definitions

- **PA (Prior Authorization)** — Payer requirement to approve certain medications before dispensing
- **PBM (Pharmacy Benefit Manager)** — Organizations that manage prescription drug benefits for health plans (e.g., Prime Therapeutics, Express Scripts, CVS Caremark, OptumRx)
- **Specialty Drug** — High-cost medications used to treat complex, chronic conditions (oncology, biologics, GLP-1s)
- **First-Pass Approval** — PA approved on initial submission without requiring additional information
- **Step Therapy** — Requirement to try and fail preferred medications before a requested drug is covered
- **Peer-to-Peer (P2P)** — Direct discussion between prescribing physician and PBM medical director to appeal a denial

---

## Contact

**Hamel Mesfin**
Co-Founder & CEO
Email: <hamel@gojjotech.com>
Phone: +1 (404) 784-0265

---

**FirstPass Rx** — *Get it right the first time.*

*Confidential — January 2026*
