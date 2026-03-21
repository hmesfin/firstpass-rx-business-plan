# Task 3 — High-Value PA Drug Targets: Summary Findings

**Data sources:** Jan 2026 Formulary PA rates x CY2023 Part D Prescribers by Provider & Drug
**Coverage:** 885 drugs matched (83.7% of all Part D claims by volume)

---

## Key Findings

### The Priority Drug Matrix

We scored every drug on two dimensions — PA requirement rate and claim volume — to identify where FirstPass Rx can create the most impact:

| Quadrant | Criteria | # Drugs | Claims | Spend |
|---|---|---|---|---|
| **Top Priority** | PA >= 50%, volume >= median | 86 | 53.5M | **$67.0B** |
| **Specialty Focus** | PA >= 50%, volume < median | 207 | 1.1M | $8.5B |
| Monitor | PA < 50%, volume >= median | 357 | — | — |
| Deprioritize | PA < 50%, volume < median | 235 | — | — |

**$75.5 billion** in annual Part D drug spend is gated behind PA requirements. That's the total addressable market for PA automation.

---

## Top 20 "Worth Fighting For" Drugs

Ranked by PA Burden Score (PA rate x claim volume):

| Rank | Drug | PA Rate | Annual Claims | Annual Spend | $/Claim | Clinical Area |
|---|---|---|---|---|---|---|
| 1 | **Semaglutide** (Ozempic/Rybelsus/Wegovy) | 100% | 7.2M | $9.7B | $1,349 | GLP-1 / Diabetes+Obesity |
| 2 | **Dulaglutide** (Trulicity) | 100% | 4.9M | $6.7B | $1,374 | GLP-1 / Diabetes |
| 3 | **Memantine** | 86% | 5.0M | $260M | $52 | Alzheimer's |
| 4 | **Cyclobenzaprine** | 54% | 5.8M | $64M | $11 | Muscle relaxant |
| 5 | **Methylprednisolone** | 58% | 4.4M | $42M | $10 | Corticosteroid |
| 6 | **Ondansetron** (combined) | 88% | 5.7M | $92M | $16 | Anti-emetic |
| 7 | **Hydroxyzine** | 52% | 3.3M | $68M | $20 | Antihistamine/Anxiolytic |
| 8 | **Tirzepatide** (Mounjaro) | 100% | 1.5M | $2.0B | $1,292 | GLP-1 / Diabetes+Obesity |
| 9 | **Cyclosporine** (Restasis) | 83% | 1.6M | $1.6B | $944 | Immunosuppressant/Ophthalmic |
| 10 | **Evolocumab** (Repatha) | 96% | 1.2M | $1.0B | $868 | PCSK9 / Cholesterol |
| 11 | **Adalimumab** (Humira) | 99% | 545K | $4.9B | $8,955 | TNF inhibitor / Immunology |
| 12 | **Lidocaine** (Lidoderm) | 60% | 909K | $160M | $176 | Topical analgesic |
| 13 | **Alirocumab** (Praluent) | 100% | 448K | $362M | $809 | PCSK9 / Cholesterol |
| 14 | **Liraglutide** (Victoza) | 100% | 426K | $617M | $1,450 | GLP-1 / Diabetes |
| 15 | **Dupilumab** (Dupixent) | 100% | 351K | $1.4B | $3,898 | IL-4/13 / Dermatology |
| 16 | **Mycophenolate mofetil** (CellCept) | 100% | 343K | $50M | $145 | Immunosuppressant |
| 17 | **Tacrolimus** (Prograf) | 86% | 397K | $85M | $213 | Immunosuppressant |
| 18 | **Etanercept** (Enbrel) | 98% | 332K | $2.6B | $7,682 | TNF inhibitor |
| 19 | **Lenalidomide** (Revlimid) | 98% | 293K | $4.8B | $16,456 | Oncology |
| 20 | **Abiraterone** (Zytiga) | 84% | 290K | $808M | $2,781 | Oncology |

---

## Clinical Themes

The Top Priority drugs cluster into clear therapeutic stories:

### 1. GLP-1 Receptor Agonists — The Elephant in the Room
Semaglutide, dulaglutide, tirzepatide, and liraglutide together represent **$19.0B in annual spend** with 100% PA rates. These are the drugs driving Part D costs and PA volume more than any other class. Every pharmacist in America is fighting these PAs daily.

### 2. Biologics & Immunosuppressants
Adalimumab ($4.9B), etanercept ($2.6B), dupilumab ($1.4B), cyclosporine ($1.6B) — all near-100% PA. These are the autoimmune/immunology workhorses where PA documentation is complex and clinical criteria are specific. High $/claim makes each approval extremely valuable.

### 3. Oncology
Lenalidomide ($4.8B, 98% PA), abiraterone ($808M, 84% PA) — and 281 additional antineoplastics in the Specialty Focus quadrant. Oncology PA is clinically urgent and high-stakes.

### 4. PCSK9 Inhibitors
Evolocumab ($1.0B) and alirocumab ($362M) — both near-100% PA. These cholesterol drugs have notoriously burdensome PA with lab value requirements.

### 5. High-Volume Generics with Moderate PA
Memantine (86% PA, 5M claims), ondansetron (88% PA, 5.7M claims), cyclobenzaprine (54% PA, 5.8M claims) — low cost per claim but massive volume means the cumulative staff time burden is enormous.

---

## Value Proposition Model

Based on **$75.5B** in PA-gated annual Part D spend:

| Denial Rate | Improvement | Annual Value Recovered |
|---|---|---|
| 10% | 10% | **$755M** |
| 15% | 20% | **$2.3B** |
| 20% | 30% | **$4.5B** |

Even at conservative assumptions (10% denial rate, 10% improvement), the addressable market for PA approval improvement is **$755 million annually** in Medicare Part D alone.

---

## Brand vs. Generic PA Patterns

Among matched drugs:
- Branded drugs with no generic equivalent (GLP-1s, biologics) have the highest PA rates — near 100%
- Generic drugs with moderate PA (memantine, ondansetron, cyclobenzaprine) represent high-volume, low-cost PA opportunities — the "death by a thousand cuts" for pharmacy staff
- The split is roughly: **high-value/low-volume** (brands/biologics) vs. **low-value/high-volume** (generics) — FirstPass Rx should optimize for both

---

## Output Files

| File | Description |
|---|---|
| `priority_drug_matrix.csv` | 885 drugs with PA rate, claims, spend, cost/claim, PA Burden Score, priority quadrant, therapeutic category |
