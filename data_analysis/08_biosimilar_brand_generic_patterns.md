# Task 8 — Biosimilar & Brand/Generic PA Patterns: Summary Findings

**Data sources:** Jan 2026 Formulary PUF with RXNORM drug type classification, CY2023 prescriber cost data
**Coverage:** 5,325 drugs (2,149 brand, 2,851 generic, 325 packs)

---

## Key Findings

### Brand Drugs Face 3x the PA Rate of Generics

| Drug Type | Drugs | Mean PA Rate | Median PA Rate |
|---|---|---|---|
| **Brand** | 2,149 | **51.4%** | 58.6% |
| **Generic** | 2,851 | **16.1%** | 0.0% |
| Brand Pack | 271 | 41.3% | 1.3% |
| Generic Pack | 54 | 20.0% | 0.0% |

The **35.3 percentage point PA premium** for brands over generics is the clearest structural pattern in the data. The median generic drug has 0% PA — most generics sail through without restriction. The median brand drug has 58.6% PA — more than half of plans require PA.

This makes economic sense: PBMs use PA to gatekeep expensive branded drugs while allowing cheap generics through. But it also means the drugs that need PA are disproportionately the expensive, complex ones where PA documentation is most burdensome.

### PA Rate Rises Steeply with Drug Cost

| Cost Tier | Drugs | Mean PA Rate | Median PA Rate | Total Spend |
|---|---|---|---|---|
| <$50/claim | 218 | 8.3% | 0.0% | $17.6B |
| $50-200 | 184 | 12.9% | 0.0% | $4.9B |
| $200-1K | 190 | 22.5% | 0.6% | $45.7B |
| **$1K-5K** | 113 | **48.4%** | 54.1% | $39.6B |
| **>$5K** | 177 | **85.7%** | **97.7%** | $43.2B |

**Drugs costing >$5,000 per claim have an 85.7% PA rate.** The pattern is nearly monotonic — the more expensive the drug, the more likely it requires PA. This creates a vicious cycle: the drugs with the most complex PA requirements are also the ones where each approval is most valuable and each denial is most harmful.

---

## Biosimilar vs Reference Biologic PA Patterns

### Adalimumab (Humira) — The Flagship Example

| Product | Type | PA Rate | Plans Carrying |
|---|---|---|---|
| **Humira** | Reference | **100%** | ~2,245 |
| Hadlima | Biosimilar | **100%** | ~2,424 |
| Cyltezo | Biosimilar | **100%** | ~479 |
| Simlandi | Biosimilar | **99%** | ~1,046 |
| Yuflyma | Biosimilar | **100%** | ~516 |
| Hyrimoz | Biosimilar | **100%** | ~14 |
| **Amjevita** | Biosimilar | **16%** | ~136 |

**Biosimilars do NOT escape PA.** In the adalimumab market, Humira and most of its biosimilars all have 100% PA rates. The biosimilar was supposed to reduce cost and improve access — instead, plans slapped the same PA requirements on them. Amjevita is the notable exception at 16% PA, but it's only on ~136 plans.

### Insulin Glargine — The Opposite Pattern

| Product | Type | PA Rate | Plans Carrying |
|---|---|---|---|
| **Lantus** | Reference | **0%** | ~4,513 |
| Basaglar | Biosimilar | **20%** | ~41 |
| Rezvoglar | Biosimilar | **15%** | ~55 |

Here the reference product (Lantus) has zero PA while the biosimilars actually face *more* PA friction on fewer plans. Plans have established Lantus as the preferred product and are using PA to steer patients away from biosimilars — the opposite of what biosimilar policy intended.

### Pegfilgrastim (Neulasta) — PA for Everyone

| Product | Type | PA Rate | Plans Carrying |
|---|---|---|---|
| **Neulasta** | Reference | **96%** | ~1,377 |
| Udenyca | Biosimilar | **96%** | ~2,151 |
| Fulphila | Biosimilar | **85%** | ~1,535 |
| Nyvepria | Biosimilar | **89%** | ~1,023 |
| Ziextenzo | Biosimilar | **97%** | ~228 |
| Fylnetra | Biosimilar | **98%** | ~52 |

The entire pegfilgrastim market — reference and biosimilars alike — is locked behind near-universal PA. Biosimilar competition hasn't reduced the PA barrier at all.

---

## The Biosimilar PA Paradox

The data reveals a fundamental problem: **biosimilars were supposed to reduce cost and improve access, but they inherit the same PA walls as the reference products.** In many cases, they face *additional* PA because plans use PA to enforce preferred product selection within the biosimilar market itself.

This creates a triple frustration for prescribers:
1. The reference biologic requires PA
2. The biosimilar requires PA too
3. If the patient is switched from one to another, that's *another* PA

For FirstPass Rx, this means the biosimilar market is a **high-value PA automation target** — the drugs are expensive, the PA criteria are complex but standardized, and the volume of PA requests is multiplied by the growing number of biosimilar options.

---

## Implications for FirstPass Rx

1. **Brand drugs are the PA battleground:** 51.4% mean PA rate vs 16.1% for generics. Focus automation on branded/specialty drugs.

2. **Cost correlates with PA:** >$5K drugs have 85.7% PA rates. These are the highest-value approvals — each successful PA is worth thousands of dollars.

3. **Biosimilars don't fix PA:** Don't assume biosimilar availability reduces PA burden. It often increases it by adding more products that each require PA.

4. **The adalimumab market is a showcase:** 7 products, all at ~100% PA, high cost per claim ($8,955). Perfect for demonstrating PA automation value — standardized criteria across a complex multi-product market.

---

## Output Files

| File | Description |
|---|---|
| `brand_vs_generic_pa_rates.csv` | 5,325 drugs with brand/generic classification and PA rates |
