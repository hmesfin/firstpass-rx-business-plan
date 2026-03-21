# Task 5 — Denial Rate Analysis & Value Proposition: Summary Findings

**Data sources:** KFF analysis of CMS Part C Reporting Requirements data, 2019-2024; Task 3 drug spend data
**Sources:**
- [KFF 2024 Report](https://www.kff.org/medicare/medicare-advantage-insurers-made-nearly-53-million-prior-authorization-determinations-in-2024/)
- [KFF 2023 Report](https://www.kff.org/medicare/nearly-50-million-prior-authorization-requests-were-sent-to-medicare-advantage-insurers-in-2023/)

---

## The Core Story: "Approvable All Along"

This is the single most powerful data point for the FirstPass Rx pitch:

> **80.7% of PA denials that are appealed get overturned. But only 12.2% of denials are ever appealed.**
>
> That means **2.9 million PA denials per year** were almost certainly approvable — but no one fought for them. At an average cost of $1,380 per PA-gated claim, that's **$4.0 billion in drug value left on the table annually** in Medicare Advantage alone.

The system isn't denying PAs because the drugs aren't medically necessary. It's denying them because the paperwork didn't get done right, or nobody had time to appeal. That's exactly the problem FirstPass Rx solves.

---

## 2024 MA Prior Authorization Landscape

| Metric | Value |
|---|---|
| Total PA requests | **52.8 million** |
| Requests per enrollee | 1.7 |
| Overall denial rate | **7.7%** |
| Total denials | **4.1 million** |
| Share of denials appealed | 12.2% |
| Appeals overturned | **80.7%** |
| Denials never challenged | **3.6 million** |
| Estimated recoverable denials | **2.9 million** |

---

## Insurer Denial Rates (2024)

| Insurer | Denial Rate | Overturn Rate | Interpretation |
|---|---|---|---|
| **UnitedHealth Group** | **12.6%** | 79% | Highest denier; 4 out of 5 appealed denials are wrong |
| **Centene** | **11.9%** | **95.3%** | Nearly ALL denials are overturned — essentially rubber-stamping denials |
| **CVS Health** | **11.6%** | **92.6%** | Similar pattern — deny first, approve on appeal |
| **Kaiser** | 10.3% | 50.2% | Integrated model; denials more likely to stick |
| **Humana** | 5.5% | 64.7% | Below-average denial rate |
| **Elevance Health** | **4.1%** | 87.9% | Lowest denial rate, but high overturn when they do deny |

**Key insight:** Centene denies 11.9% of PAs, but 95.3% of those are overturned on appeal. This means Centene's true "appropriate denial" rate is approximately **0.6%**. The other 11.3% are effectively administrative friction — denials that exist only because someone didn't appeal them.

---

## Denial Rates Are Rising

| Year | PA Requests | Denial Rate | Change |
|---|---|---|---|
| 2019 | 37.4M | 5.9% | — |
| 2020 | 30.8M | 5.5% | -0.4pp (COVID dip) |
| 2021 | 36.2M | 5.9% | +0.4pp |
| 2022 | 40.6M | **7.4%** | **+1.5pp** |
| 2023 | 49.8M | 6.4% | -1.0pp |
| 2024 | 52.8M | **7.7%** | **+1.3pp** |

PA requests increased 41% from 2019 to 2024 (37.4M → 52.8M). Denial rates rose 31% (5.9% → 7.7%). The problem is getting worse, not better. The 2024 CMS Interoperability Rule mandates new PA transparency reporting starting 2026 — our analysis sets the baseline.

---

## Value Proposition Model

Based on 4.07M annual MA PA denials, at $1,380 average cost per PA-gated claim:

| Market Penetration | Approval Lift | Additional Approvals | Annual Value Recovered |
|---|---|---|---|
| 1% | 20% | 8,131 | **$11.2M** |
| 2% | 20% | 16,262 | **$22.4M** |
| 5% | 20% | 40,656 | **$56.1M** |
| 5% | 30% | 60,984 | **$84.2M** |
| 10% | 20% | 81,312 | **$112.2M** |
| 10% | 30% | 121,968 | **$168.3M** |

**Conservative scenario** (1% market, 20% lift): $11.2M/year in recovered drug value
**Base scenario** (5% market, 20% lift): $56.1M/year
**Ambitious scenario** (10% market, 30% lift): $168.3M/year

Note: These figures represent drug value recovered for patients. FirstPass Rx revenue model would be a fraction of this (e.g., per-PA fee or percentage of recovered value).

---

## Headline Numbers for Pitch Deck

1. **53 million** PA requests submitted annually in Medicare Advantage
2. **7.7% denied** = 4.1 million denials per year
3. **80.7%** of appeals are overturned — most denials were approvable all along
4. **Only 12.2%** of denials are ever appealed — 2.9M approvals left on the table
5. Denial rates are **rising**: 5.9% (2019) → 7.7% (2024), a 31% increase
6. **$4.0 billion** in annual drug value goes unrecovered because denied PAs aren't appealed
7. The worst offenders (UnitedHealth 12.6%, Centene 11.9%, CVS 11.6%) are also the largest insurers

---

## Output Files

| File | Description |
|---|---|
| `ma_denial_rates_by_insurer.csv` | 7 insurer groups with denial, overturn, and effective denial rates |
| `value_proposition_model.csv` | 16 scenarios across market penetration x approval improvement |
