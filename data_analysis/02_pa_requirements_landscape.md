# Task 1 — PA Requirement Landscape: Summary Findings

**Data source:** CMS Part D Formulary PUF, January 2026 (contract year 2026)
**Coverage:** 1,118,219 drug-formulary records across 5,086 plans (331 unique formularies), 5,994 unique drugs

---

## Key Findings

### Overall Utilization Management Rates

Across all drug-formulary records in Part D:

| UM Tool | Rate |
|---|---|
| **Prior Authorization** | **28.1%** |
| Quantity Limits | 38.8% |
| Step Therapy | 1.0% |

Over one in four drug-plan combinations require PA. Quantity limits are even more prevalent, but PA is the primary access barrier that requires clinical staff intervention.

### Scale of the PA Problem

- **5,325 drugs** appear on 10+ plans (our analysis universe after noise filtering)
- **1,349 drugs (25%)** have "universal PA" — required by 80%+ of plans that carry them
- **464 drugs (9%)** are "split" drugs (30-70% PA rate) — representing formulary arbitrage opportunities where PA requirements vary widely across plans
- Of the 1,349 universal PA drugs, many are carried by all ~5,085 active plans, meaning nearly every Medicare Part D beneficiary faces PA for these medications

---

## Top 10 Therapeutic Categories by PA Burden

Ranked by **weighted PA rate** (total PA-required plan-drug instances / total plan-drug instances):

| Rank | Therapeutic Category | Weighted PA Rate | # Drugs | Key Clinical Context |
|---|---|---|---|---|
| 1 | **Other Respiratory Products** | 98.7% | 11 | Specialty inhalers, surfactants, pulmonary hypertension agents |
| 2 | **Bile and Liver Therapy** | 96.6% | 13 | UDCA, obeticholic acid — chronic liver disease management |
| 3 | **Antianemic Preparations** | 94.4% | 14 | ESAs (epoetin, darbepoetin), iron infusions — high-cost injectables with safety concerns driving PA |
| 4 | **Antiemetics and Antinauseants** | 93.3% | 15 | NK1 antagonists, 5-HT3 antagonists — oncology supportive care |
| 5 | **Other Hematological Agents** | 92.0% | 10 | Thrombopoietin agonists, factor replacements |
| 6 | **Immunosuppressants** | 90.7% | 292 | TNF inhibitors (adalimumab, etanercept), IL inhibitors, calcineurin inhibitors — **largest category by drug count**; includes biologics and biosimilars |
| 7 | **Antineoplastic Agents** | 90.1% | 281 | Oral oncology (kinase inhibitors, hormonal agents) — **second largest category**; nearly all require PA |
| 8 | **Antihemorrhagics** | 85.4% | 25 | Factor replacements, thrombopoietin agonists |
| 9 | **Pituitary/Hypothalamic Hormones** | 84.8% | 70 | Growth hormone, GnRH analogs, octreotide — high-cost specialty drugs |
| 10 | **Immunostimulants** | 84.6% | 39 | Interferons, colony-stimulating factors (G-CSF) |

**Observation:** The top PA categories heavily overlap with specialty pharmacy and biologics. Immunosuppressants (292 drugs) and Antineoplastics (281 drugs) together account for **573 drugs** — over half the universal PA universe. This aligns with the MN PBM Transparency Report finding that Immunological Agents were the #1 spend category.

---

## Universal PA Drugs (80%+ PA Rate): Notable Examples

These drugs require PA on virtually every plan that carries them:

**Immunosuppressants/Biologics:**
- Tacrolimus (all oral forms) — 100% PA, 5,085 plans
- Mycophenolate mofetil — 100% PA, 5,085 plans
- Sirolimus, everolimus — 100% PA, 5,085 plans
- Sarilumab (Kevzara), benralizumab (Fasenra), tildrakizumab (Ilumya)

**Oncology:**
- Nilotinib (Tasigna), everolimus — 100% PA
- Broad sweep across kinase inhibitors

**Specialty:**
- Somatropin (Nutropin) — growth hormone, 100% PA
- Dornase alfa (Pulmozyme) — cystic fibrosis, 100% PA
- Alpha-1 proteinase inhibitor (Zemaira) — 100% PA

---

## Split Drugs (30-70% PA Rate): Formulary Arbitrage Opportunities

These are drugs where PA requirements vary significantly across plans — meaning some PBMs require PA while others don't, creating opportunities for plan selection and PA strategy:

**High-volume split drugs (carried by 5,085 plans):**
- Calcitriol (vitamin D analog) — 31% PA
- Prednisolone oral solution — 32% PA
- Morphine sulfate ER — 33% PA
- Iloperidone (Fanapt) — 66% PA
- Vericiguat (Verquvo) — 68% PA
- Desipramine — 33% PA

These split drugs are interesting for FirstPass Rx because the variation in PA requirements across plans suggests the PA decision is not clinically driven — it's a formulary management choice. This is where PA automation and appeal optimization can have the highest marginal impact.

---

## Data Quality Notes

- **ATC classification coverage:** 88% of formulary drugs matched to ATC therapeutic categories via RXNREL ingredient chain resolution
- **Unmatched drugs (~12%):** Primarily combination products, packs, vaccines, and medical devices without clean ATC mappings
- **Plan counting:** PA rates are weighted by the number of plans using each formulary (multiple plans can share one formulary ID)
- **Data vintage:** January 2026 formulary snapshot; formularies update monthly

---

## Output Files

| File | Description |
|---|---|
| `pa_rate_by_drug.csv` | 5,325 drugs ranked by PA rate with ATC categories (drugs on 10+ plans) |
| `pa_rate_by_category.csv` | 76 ATC therapeutic categories with weighted PA rates |
