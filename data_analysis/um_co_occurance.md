# Task 6 — UM Co-occurrence Analysis: Summary Findings

**Data source:** Jan 2026 Part D Formulary PUF, plan-weighted
**Coverage:** 5,325 drugs on 10+ plans, ~17.4M plan-drug instances

---

## Key Findings

### Overall UM Burden Distribution

| UM Pattern | Plan-Drug Instances | Share |
|---|---|---|
| **No UM restrictions** | 8,778,100 | 50.3% |
| QL Only | 3,805,040 | 21.8% |
| **PA + QL** | **3,114,246** | **17.9%** |
| PA Only | 1,624,846 | 9.3% |
| ST + QL | 95,010 | 0.5% |
| ST Only | 27,770 | 0.2% |
| PA + ST | 1,205 | <0.1% |
| PA + ST + QL (Triple) | 9 | <0.001% |

**Half of all drug-plan combinations have no UM restrictions.** Of the other half, PA + Quantity Limits is by far the most common combination.

### The PA + QL Story

Among all PA drug-plan instances:
- **65.7%** also have quantity limits — the patient needs PA approval AND is capped on how much they can get
- **34.3%** have PA only with no other restrictions
- **<0.1%** have step therapy co-occurring with PA

**Step therapy is essentially irrelevant in Part D formularies.** Only 0.7% of all drug-plan instances carry step therapy, and it almost never co-occurs with PA. This is a major difference from commercial/employer plans where step therapy is much more common.

This simplifies the FirstPass Rx product focus: **the UM battle in Medicare Part D is PA + QL, not step therapy.** The PA automation tool doesn't need to handle complex step therapy logic for this market.

### Among High-PA Drugs (>=50% PA rate)

Of the 1,660 drugs with >=50% PA rate:
- **77.2%** also have quantity limits on >=10% of plans
- **2.8%** have step therapy on >=5% of plans
- **~0%** have true triple burden

### Drugs with Highest Step Therapy Co-occurrence

The few drugs where PA + ST does co-occur are notable:

| Drug | PA Rate | ST Rate | Category |
|---|---|---|---|
| Metaxalone 400 MG | 55% | 41% | Muscle relaxant |
| Monomethyl fumarate (Bafiertam) | 64% | 36% | Multiple sclerosis |
| Asenapine (Saphris) | 64% | 36% | Atypical antipsychotic |
| Iloperidone (Fanapt) | 66% | 31% | Atypical antipsychotic |
| Methylnaltrexone (Relistor) | 66% | 30% | Opioid-induced constipation |
| Levomilnacipran (Fetzima) | 53% | 28% | SNRI antidepressant |

These are all second/third-line agents in their class — plans require the patient to "fail first" on a preferred alternative (step therapy) AND then get PA for the non-preferred drug. These represent the hardest PA approvals in Part D.

---

## Implications for FirstPass Rx

1. **Product scope:** PA + QL is the dominant combo. FirstPass Rx should handle PA as primary, with QL awareness (knowing the limit helps set expectations and avoid re-PAs for refills).

2. **Step therapy is a niche problem:** Only ~47 drugs have meaningful PA + ST co-occurrence. These are complex but low-volume — handle them as an advanced feature, not MVP.

3. **The QL dimension matters for workflow:** When a drug has PA + QL, the pharmacy may need to submit PA more frequently (e.g., if the patient needs more than the quantity limit allows, requiring a PA override). This is where automation saves repeated staff time.

---

## Output Files

| File | Description |
|---|---|
| `um_burden_by_drug.csv` | 5,325 drugs with PA/ST/QL rates and co-occurrence patterns |
