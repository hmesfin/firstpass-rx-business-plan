# Task 2 — Plan-Level PA Restrictiveness Ranking: Summary Findings

**Data source:** CMS Part D Formulary PUF + Plan Information, January 2026
**Coverage:** 5,085 plans across 330 unique formularies, mapped to 12 insurer groups

---

## Key Findings

### Overall UM Burden Across Plans

| Metric | Average Across All Plans |
|---|---|
| **PA rate** | **27.2%** of drugs require PA |
| Step therapy rate | 0.7% |
| Quantity limit rate | 40.2% |
| Restrictiveness score (0-1 composite) | 0.205 |

The typical Part D plan requires prior authorization for about 1 in 4 drugs on its formulary. Quantity limits are the most common UM tool (40%), but PA is the one that requires clinical staff intervention and creates the access barrier FirstPass Rx addresses.

### Restrictiveness Range

The spread is dramatic:
- **Most restrictive plan** (CalOptima OneCare): 38% PA rate, 0.254 score
- **Least restrictive plan** (Kaiser Permanente): 6% PA rate, 0.029 score
- That's a **6x difference** in PA burden between the most and least restrictive plans

---

## Insurer Restrictiveness Ranking

| Rank | Insurer Group | Plans | Avg PA Rate | Restrictiveness | MN Plans |
|---|---|---|---|---|---|
| 1 | **Molina Healthcare** | 13 | 33% | 0.240 | 0 |
| 2 | **HCSC (BCBS licensee)** | 29 | 30% | 0.227 | 0 |
| 3 | **Blue Cross Blue Shield (various)** | 49 | 30% | 0.224 | 0 |
| 4 | **Elevance Health (Anthem)** | 41 | 30% | 0.223 | 11 |
| 5 | **CVS Health / Aetna** | 294 | 28% | 0.212 | 9 |
| 6 | **Humana** | 384 | 26% | 0.210 | 5 |
| 7 | **Cigna / Express Scripts** | 10 | 27% | 0.201 | 0 |
| 8 | **UnitedHealth Group / OptumRx** | 253 | 25% | 0.196 | 22 |
| 9 | **Centene** | 26 | 23% | 0.182 | 0 |
| 10 | **SCAN Health Plan** | 55 | 28% | 0.159 | 0 |
| 11 | **Kaiser Permanente** | 56 | 8% | 0.042 | 0 |

**Key observations:**

- **Molina is the most restrictive** — 33% PA rate, highest composite score. Small plan count (13) but Molina is a major Medicaid/duals player.
- **BCBS entities (HCSC + various + Elevance)** collectively are the most restrictive large insurer family, with 30% PA rates across ~120 plans.
- **Kaiser is an outlier** — only 6% PA rate, nearly zero quantity limits. Their integrated model (own pharmacies, own formulary committee) means they handle UM internally rather than through PA gatekeeping.
- **UnitedHealth/OptumRx is below average** in restrictiveness (25% PA) despite being the largest Part D insurer by plan count — interesting positioning as "less burdensome."

---

## Top 10 Most Restrictive Plans (Primary FirstPass Rx Targets)

| Plan | PA Rate | ST Rate | QL Rate | Score |
|---|---|---|---|---|
| CalOptima Health OneCare Complete (HMO D-SNP) | 38% | 0% | 39% | 0.254 |
| Blue MedicareRx Value Plus (PDP) | 34% | 1% | 42% | 0.244 |
| BlueMedicare Value Rx (PDP) | 34% | 1% | 42% | 0.244 |
| Molina One Care (HMO D-SNP) | 34% | 1% | 42% | 0.240 |
| Senior Whole Health SCO (HMO D-SNP) | 34% | 1% | 42% | 0.240 |
| Senior Whole Health SCO NHC (HMO D-SNP) | 34% | 1% | 42% | 0.240 |
| Molina Medicare Complete Care (HMO D-SNP) | 33% | 1% | 42% | 0.240 |
| Molina Medicare Complete Care Plus (HMO D-SNP) | 33% | 1% | 42% | 0.240 |
| Molina Medicare Complete Care Select (HMO D-SNP) | 33% | 1% | 42% | 0.240 |
| Molina Medicare Complete Care Plus (HMO D-SNP) | 33% | 1% | 42% | 0.240 |

Notable pattern: **D-SNP plans (dual-eligible special needs)** dominate the most restrictive list. These serve the most vulnerable beneficiaries — low-income seniors eligible for both Medicare and Medicaid — yet impose the highest PA burden.

---

## Minnesota Market View

**63 plans** operate in Minnesota, spanning 5 insurer groups:

| MN Rank | Plan | PA Rate | Score | Insurer |
|---|---|---|---|---|
| 1 | IMCare Classic (HMO D-SNP) | 33% | 0.239 | Other |
| 2 | Platinum Blue Core Plan with Rx (Cost) | 30% | 0.229 | BCBS |
| 3 | Blue Cross Medicare Advantage Core (PPO) | 30% | 0.229 | BCBS |
| 4 | Blue Cross Medicare Advantage Comfort (PPO) | 30% | 0.229 | BCBS |
| 5 | Blue Cross Medicare Advantage Complete (PPO) | 30% | 0.226 | BCBS |

**UnitedHealth Group / OptumRx** has the largest MN presence (22 plans), followed by Elevance/Anthem (11), CVS/Aetna (9), and Humana (5). Blue Cross dominates the top restrictiveness positions in MN.

For pilot targeting: **Blue Cross plans in MN** are the highest-PA payer — pharmacists submitting PAs to BCBS plans face the most friction and would benefit most from FirstPass Rx.

---

## Restrictiveness Score Methodology

The composite score weights the three UM tools by clinical burden:

```
Score = (PA_rate * 3 + ST_rate * 2 + QL_rate * 1) / 6
```

- **PA (weight 3):** Requires clinical documentation and staff time — the primary access barrier
- **Step Therapy (weight 2):** Requires patient to fail alternative first — delays treatment
- **Quantity Limits (weight 1):** Administrative but less burdensome — often handled at pharmacy level

---

## Output Files

| File | Description |
|---|---|
| `plan_pa_restrictiveness.csv` | 5,085 plans ranked by restrictiveness with PA/ST/QL rates, insurer group, MN flag |
| `insurer_pa_ranking.csv` | 12 insurer groups with averaged and weighted restrictiveness metrics |
