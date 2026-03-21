# Task 4 — Prescriber Targeting Intelligence: Summary Findings

**Data sources:** CY2023 Part D Prescribers by Provider & Drug, tagged with Jan 2026 Formulary PA rates
**Coverage:** 26.8M prescriber-drug records, 1.6M rows involving high-PA drugs (>=50% PA rate)

---

## Key Findings

### Who Is Fighting the Most PAs?

The top 5 specialties by PA-weighted claim volume:

| Rank | Specialty | PA Claims | PA Cost | Prescribers | PA Share of Rx |
|---|---|---|---|---|---|
| 1 | **Family Practice** | 8.7M | $6.1B | 103,916 | 2.4% |
| 2 | **Internal Medicine** | 8.2M | $8.1B | 102,764 | 2.5% |
| 3 | **Nurse Practitioner** | 8.0M | $10.1B | 211,300 | 3.4% |
| 4 | **Physician Assistant** | 3.2M | $4.3B | 106,533 | 3.8% |
| 5 | **Endocrinology** | 2.2M | $3.5B | 6,407 | **12.9%** |

**The story is two-fold:**

- **Primary care** (Family Practice, Internal Medicine, NPs, PAs) generates the highest absolute PA volume — 28.9M PA-weighted claims — because they prescribe everything. But PA is only 2-4% of their total Rx volume, so it's a diffuse burden spread across many drugs.
- **Specialists** generate less absolute volume (15.7M PA claims) but face much higher PA concentration. Endocrinology (12.9%), Hematology-Oncology (19.0%), and Rheumatology (12.5%) have the highest PA share — meaning more than 1 in 8 prescriptions they write hits a PA wall.

### The Specialist PA Pain Points

| Specialty | PA Share | PA Cost | Why |
|---|---|---|---|
| **Hematology-Oncology** | 19.0% | $11.5B | Oral oncology, lenalidomide, ibrutinib |
| **Endocrinology** | 12.9% | $3.5B | GLP-1s (semaglutide, tirzepatide, dulaglutide) |
| **Rheumatology** | 12.5% | $6.8B | TNF inhibitors (adalimumab, etanercept), IL inhibitors |
| **Neurology** | 10.0% | $2.8B | Memantine, MS drugs, anti-epileptics |
| **Gastroenterology** | 6.0% | $2.5B | Biologics for IBD, liver disease |
| **Dermatology** | 6.0% | $1.9B | Dupilumab, biologics for psoriasis |

---

## Primary Care vs. Specialist: Where Should FirstPass Rx Start?

| Segment | PA Claims | PA Cost | Prescribers |
|---|---|---|---|
| **Primary Care** | 28.9M | $28.9B | 534,156 |
| **Specialist** | 15.7M | $43.6B | 570,006 |

Primary care has **2x the PA claim volume** but specialists have **1.5x the PA dollar value**. The per-prescriber PA burden is much higher for specialists:

- Average specialist: 27.5 PA claims/year
- Average primary care provider: 54.1 PA claims/year
- Average endocrinologist: **336 PA claims/year**
- Average rheumatologist: **256 PA claims/year**
- Average hematologist-oncologist: **154 PA claims/year**

**Recommendation:** Start with **endocrinology and rheumatology** for pilot — they have the highest per-provider PA burden, the drugs are well-defined (GLP-1s, TNF inhibitors), and the PA criteria are standardized enough for automation.

---

## Geographic Analysis

### Top 10 States by PA Burden

| Rank | State | PA Claims | PA Cost | Prescribers |
|---|---|---|---|---|
| 1 | CA | 3.95M | $7.1B | 110,430 |
| 2 | FL | 3.57M | $5.0B | 75,160 |
| 3 | TX | 3.39M | $5.2B | 72,735 |
| 4 | NY | 2.99M | $6.0B | 77,179 |
| 5 | PA | 2.03M | $3.5B | 50,761 |
| 6 | OH | 1.79M | $2.8B | 43,651 |
| 7 | NC | 1.73M | $2.7B | 36,475 |
| 8 | GA | 1.62M | $2.4B | 29,830 |
| 9 | MI | 1.44M | $2.6B | 37,055 |
| 10 | IL | 1.37M | $2.4B | 41,150 |

Follows Medicare enrollment — large states with older populations dominate.

### Minnesota Detail

- **State rank:** #25 of 62 by PA burden volume
- **PA-weighted claims:** 561,144
- **PA-weighted cost:** $1.06B
- **Prescribers:** 20,604

**MN Top Specialties by PA Burden:**

| Specialty | PA Claims | Prescribers | Per-Provider PA |
|---|---|---|---|
| Family Practice | 133,917 | 1,860 | 72/year |
| Nurse Practitioner | 95,319 | 1,781 | 54/year |
| Internal Medicine | 76,706 | 806 | 95/year |
| Physician Assistant | 58,691 | 1,235 | 48/year |
| Neurology | 23,720 | 224 | 106/year |
| Endocrinology | 21,179 | 115 | **184/year** |
| Hematology-Oncology | 16,795 | 136 | **124/year** |

**MN pilot targeting:** The 115 endocrinologists in MN handle ~21K PA claims/year (184 per provider). That's a tight, reachable market with high per-provider pain. Rheumatology (79 providers, ~163 PA claims each) is the second-best target.

---

## Pilot Targeting Recommendation: Top 5 Specialties

Based on PA burden per provider, drug standardization, and clinical urgency:

| Priority | Specialty | Why | MN Providers | PA/Provider/Year |
|---|---|---|---|---|
| 1 | **Endocrinology** | GLP-1s = highest volume, standardized PA criteria | 115 | 184 |
| 2 | **Rheumatology** | TNF inhibitors, well-defined step therapy | 79 | ~163 |
| 3 | **Hematology-Oncology** | Highest $/claim, clinical urgency | 136 | 124 |
| 4 | **Neurology** | Memantine (huge volume), MS drugs | 224 | 106 |
| 5 | **Internal Medicine** | Broad PA volume, GLP-1 + immunosuppressant mix | 806 | 95 |

---

## Output Files

| File | Description |
|---|---|
| `pa_burden_by_specialty.csv` | All specialties with PA-weighted claims, cost, prescriber count |
| `pa_volume_by_state.csv` | All states with PA burden, MN flagged |
| `top_prescriber_specialties.csv` | Top 20 specialties for targeting |
