# FirstPass Rx — CMS Data Analysis: Findings Summary

## The Scale of the Prior Authorization Problem in Medicare Part D

Prior authorization is the dominant access barrier in Medicare Part D. Our analysis of the January 2026 CMS Formulary PUF — covering 5,086 plans, 330 formularies, and 5,994 unique drugs — reveals a system that systematically delays or denies medically necessary medications:

- **28.1%** of all drug-plan combinations require prior authorization
- **1,349 drugs** (25% of all drugs on 10+ plans) have near-universal PA — required by 80%+ of plans
- **$75.5 billion** in annual Part D drug spend is gated behind PA requirements
- PA rates are **rising**: from 5.9% denial rate in 2019 to 7.7% in 2024

The 3.7GB Part D Prescribers dataset (CY2023, 26.8M records) confirms the burden falls unevenly: endocrinologists face 184 PA claims per year, rheumatologists 163, and hematologist-oncologists 154. Meanwhile, 80.7% of appealed denials are overturned — most denied PAs were approvable all along. But only 12.2% of denials are ever appealed, leaving an estimated **2.9 million approvals** and **$4.0 billion in drug value** on the table annually.

---

## Top 10 Drug Classes by PA Burden

| Rank | Therapeutic Category | PA Rate | Drugs | Key Examples |
|---|---|---|---|---|
| 1 | Other Respiratory Products | 98.7% | 11 | Specialty inhalers, surfactants |
| 2 | Bile and Liver Therapy | 96.6% | 13 | Obeticholic acid, UDCA |
| 3 | Antianemic Preparations | 94.4% | 14 | ESAs (epoetin), iron infusions |
| 4 | Antiemetics/Antinauseants | 93.3% | 15 | NK1 antagonists, 5-HT3 agents |
| 5 | Immunosuppressants | 90.7% | 292 | Adalimumab, etanercept, tacrolimus |
| 6 | Antineoplastic Agents | 90.1% | 281 | Lenalidomide, abiraterone, kinase inhibitors |
| 7 | Antihemorrhagics | 85.4% | 25 | Factor replacements, TPO agonists |
| 8 | Pituitary/Hypothalamic Hormones | 84.8% | 70 | Growth hormone, GnRH analogs |
| 9 | Immunostimulants | 84.6% | 39 | Interferons, G-CSF |
| 10 | Musculoskeletal (Other) | 80.8% | 8 | Specialty anti-inflammatory agents |

Immunosuppressants (292 drugs) and antineoplastics (281 drugs) together account for 573 drugs — over 40% of the universal PA universe.

---

## Top 5 Most Restrictive Payers

| Rank | Insurer | Avg PA Rate | Denial Rate (MA) | Overturn Rate | Notes |
|---|---|---|---|---|---|
| 1 | **Molina Healthcare** | 33% | N/A | N/A | Highest formulary PA rate; D-SNP focus |
| 2 | **HCSC (BCBS licensee)** | 30% | N/A | N/A | Major BCBS operator |
| 3 | **Blue Cross Blue Shield (various)** | 30% | N/A | N/A | Includes BCBS of MN |
| 4 | **UnitedHealth Group / OptumRx** | 25% | **12.6%** | 79% | Highest MA denial rate nationally |
| 5 | **CVS Health / Aetna** | 28% | **11.6%** | 93% | 93% of appealed denials overturned |

Kaiser Permanente is a dramatic outlier at just 6% PA rate — their integrated model handles UM internally. The 6x spread between most and least restrictive plans demonstrates that PA is a payer choice, not a clinical necessity.

---

## The Minnesota Market Opportunity

Minnesota is a strong pilot market with $1.06 billion in PA-gated drug cost:

- **63 plans** operate in MN across 16 formularies
- **MN PA rate (28.1%)** matches the national average — the problem is just as acute
- **GLP-1s alone** represent $247M in MN PA-gated cost (semaglutide: $133M, dulaglutide: $84M)
- **Rochester** (Mayo Clinic) has nearly as many prescribers as Minneapolis — high specialty density
- MN has a uniquely local payer mix (Medica, HealthPartners, BCBSM) enabling direct relationships

**Pilot target:** 115 MN endocrinologists (184 PAs/year each) + 79 rheumatologists (~163 PAs/year each), focused on Minneapolis/St. Paul metro + Rochester, targeting GLP-1 and TNF inhibitor PAs.

The MN PBM Transparency Report's top spend categories — Immunological Agents (92% PA rate), Antineoplastics (91%), Blood Glucose Regulators — align perfectly with the highest PA burden categories, validating the market opportunity.

---

## Key Statistics for the FirstPass Rx Value Proposition

| Metric | Value | Source |
|---|---|---|
| Annual MA PA requests | **52.8 million** | KFF/CMS 2024 |
| Overall denial rate | **7.7%** | KFF/CMS 2024 |
| Appeal overturn rate | **80.7%** | KFF/CMS 2024 |
| Share of denials appealed | **12.2%** | KFF/CMS 2024 |
| Recoverable denials/year | **2.9 million** | Calculated |
| PA-gated annual drug spend | **$75.5 billion** | Task 3 analysis |
| Drug value left on table | **$4.0 billion/year** | Calculated |
| Brand drug PA rate | **51.4%** | Task 8 analysis |
| Generic drug PA rate | **16.1%** | Task 8 analysis |
| Drugs >$5K/claim PA rate | **85.7%** | Task 8 analysis |

The most damning statistic: **Centene denies 11.9% of PAs, but 95.3% are overturned on appeal.** Their true "appropriate denial" rate is approximately 0.6%. The rest is pure administrative friction.
