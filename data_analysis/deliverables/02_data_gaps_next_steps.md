# FirstPass Rx — Data Gaps & Next Steps

## What We Could NOT Find in Public Data

### 1. Claim-Level PA Outcomes
**Gap:** The formulary PUF tells us which drugs *require* PA, but not whether PAs are approved or denied at the individual claim level. We know the PA rate but not the approval rate per drug.

**Why it matters:** To build the automation engine, we need to know which PA criteria lead to approvals vs denials, and what documentation patterns succeed.

**How to get it:**
- **ResDAC/CCW Data Use Agreement (DUA):** The Part D Event (PDE) file contains a PA flag at the claim level. Requires a formal DUA application (~3-6 month process, academic or research affiliation helps).
- **Direct PBM data partnerships:** Negotiate data-sharing agreements with OptumRx, CVS Caremark, or Medica for PA decision data in exchange for analytics/value.

### 2. PA Criteria and Clinical Requirements
**Gap:** We know *that* a drug requires PA, but not *what* the PA criteria are (e.g., lab values, prior therapies, diagnosis codes required).

**Why it matters:** This is the core of what FirstPass Rx needs to automate — the actual PA submission requirements.

**How to get it:**
- **CMS Coverage Analysis Tool:** CMS publishes some coverage determination criteria, but it's not comprehensive.
- **PBM formulary PA criteria documents:** These are technically available to prescribers but not in structured, machine-readable format. Scraping or partnerships needed.
- **CoverMyMeds / Surescripts PA criteria data:** Commercial PA platforms have this data; potential partnership or competitor analysis.

### 3. Plan Enrollment Data
**Gap:** We used county coverage as a proxy for plan size, but don't have actual beneficiary enrollment by plan.

**Why it matters:** Weighting PA burden by enrollment tells us which plans affect the most patients.

**How to get it:**
- **CMS Monthly Enrollment by CPSC:** Published monthly at data.cms.gov, contains plan-level enrollment counts. We should download and incorporate this.

### 4. MA PA Denial Data by Drug Category
**Gap:** KFF data gives us insurer-level denial rates, but not broken down by drug category. We can't say "UnitedHealth denies 25% of GLP-1 PAs" — only that they deny 12.6% overall.

**Why it matters:** Drug-specific denial rates would sharpen the value proposition for each therapeutic area.

**How to get it:**
- **CMS Part C Reporting Requirements raw data:** The underlying data behind the KFF analysis may contain more granularity. FOIA request or direct download from CMS.
- **OIG reports:** HHS Office of Inspector General periodically publishes drug-specific MA denial analyses.

### 5. Time-to-Decision Data
**Gap:** We have no data on how long PAs take to process — from submission to approval/denial.

**Why it matters:** Time-to-approval is a core part of the FirstPass Rx value proposition. Reducing a 5-day wait to same-day is clinically meaningful.

**How to get it:**
- **2024 CMS Interoperability Rule:** Starting 2026, MA plans must report PA processing times via HL7 FHIR APIs. This data will become available as plans implement the mandate.
- **Pharmacy management system data:** Partners like pharmacies and EHR vendors may have time-to-decision data from their PA submission workflows.

### 6. Minnesota-Specific Claims Data
**Gap:** MN prescriber data is available by state, but MN-specific plan-level PA outcome data is not public.

**Why it matters:** Sharpens the MN pilot market sizing and targeting.

**How to get it:**
- **MN Commerce Department MGDPA Request:** Minnesota's Managed Care Data Governance and Practice Act may allow access to plan-level PA data for MN-licensed plans.
- **MN All-Payer Claims Database (MN APCD):** Operated by MN Department of Health, contains claims data that may include PA flags. Requires application.

---

## Recommended Next Steps (Priority Order)

| Priority | Action | Timeline | Value |
|---|---|---|---|
| 1 | **Download CMS Monthly Enrollment by CPSC** | 1 day | Weight PA burden by actual enrollment |
| 2 | **Apply for ResDAC/CCW DUA** | 3-6 months | Claim-level PA outcome data |
| 3 | **Scrape PBM PA criteria documents** | 2-4 weeks | Build the PA automation knowledge base |
| 4 | **Apply to MN APCD** | 1-3 months | MN-specific claims with PA flags |
| 5 | **Monitor 2026 CMS FHIR PA APIs** | Ongoing | Real-time PA processing data as it becomes available |
| 6 | **Approach CoverMyMeds for partnership** | Ongoing | Commercial PA criteria data + workflow integration |

---

## What This Analysis DID Accomplish

Despite the gaps, this analysis provides a strong foundation:

- Identified the **specific drugs, payers, specialties, and geographies** to target
- Quantified the **$75.5B addressable market** and **$4.0B in annual recoverable value**
- Validated the **MN market opportunity** with $1.06B in PA-gated cost
- Produced **pitch deck-ready statistics** from authoritative CMS sources
- Built a reusable data pipeline (RXCUI→ingredient→ATC classification) for future analysis
