# FirstPass Rx Business Plan

## What This Is

Business plan and project plan for FirstPass Rx — a specialty drug prior authorization validation service. This repo contains strategy documents, not application code.

**MVP Go Live Target: July 7, 2026**

## Repository Structure

- `00_executive_summary.md` — One-page investor/partner summary
- `01_steakholder_presentation.md` — Full stakeholder pitch deck (markdown)
- `02_project_plan.md` — Detailed project plan with phases, tasks, and status tracking
- `03_criteria_extraction_worksheet.md` / `03b_*` — PA criteria extraction templates
- `04_blank_extraction_worksheet.md` — Blank extraction worksheet for new drugs
- `05_partners_and_advisors.md` — Partner/advisor agreement outlines
- `06_example_skill.md` — Example skill document
- `data_analysis/` — CMS data analysis working files (task prompts, methodology)
- `data_analysis/deliverables/` — Final analysis outputs used in business plan:
  - `01_findings_summary.md` — Key CMS data findings
  - `02_data_gaps_next_steps.md` — Known data gaps and next steps
  - `03_value_proposition_model.csv` — Market penetration x approval improvement scenarios
  - `04_priority_drug_list.csv` — Drugs ranked by PA burden score
  - `05_target_payer_list.csv` — Payers ranked by restrictiveness score

## Key Data Points (from CMS analysis)

When updating documents, use these validated numbers:

- $75.5B annual PA-gated drug spend (CMS Formulary PUF)
- 28.1% of drug-plan combos require PA
- 80.7% appeal overturn rate (KFF/CMS 2024)
- 2.9M recoverable approvals / $4.0B left on table annually
- MN pilot market: $1.06B PA-gated cost
- Top drugs by PA burden: Semaglutide, Dulaglutide, Tirzepatide, Adalimumab

## Conventions

- Documents are numbered with prefix (`00_`, `01_`, etc.) for ordering
- Task statuses in project plan use `☐ Not Started`, `☐ **In Process**`, `☐ **Done**`
- Deliverable checklists use `[ ]` / `[x]`
- Keep all documents consistent — dates, stats, and drug lists should match across files
- When updating timeline or market data, update all three core docs (00, 01, 02)

## Important Context

- Founder (Hamel Mesfin): former VP at Prime Therapeutics, technical lead
- Clinical Lead (Yonatan Berhe): pharmacist with PBM/specialty pharmacy PA experience
- Pilot market: Minnesota (Minneapolis/St. Paul + Rochester)
- Target specialties: Endocrinology, Rheumatology, Oncology, Dermatology
- Tech stack (for the product, not this repo): Django + Vue.js on Hetzner
