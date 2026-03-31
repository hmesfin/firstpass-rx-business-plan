
# FirstPass Rx — Pre-Pilot Project Plan

## MVP Go Live Target: July 7, 2026

---

## Document Control

| Field              | Value                               |
| ------------------ | ----------------------------------- |
| **Document Title** | FirstPass Rx Pre-Pilot Project Plan |
| **Version**        | 2.0                                 |
| **Created Date**   | January 2026                        |
| **Last Updated**   | March 2026                          |
| **Owner**          | Hamel Mesfin                        |
| **Status**         | Draft                               |

---

## Executive Summary

This project plan outlines all tasks, milestones, and deliverables required to launch the FirstPass Rx MVP by July 7, 2026. The plan is organized into four phases:

| Phase | Timeline | Focus |
|-------|----------|-------|
| **Phase 1: Foundation** | January – February 2026 | Knowledge capture, infrastructure, legal setup, CMS data analysis |
| **Phase 2: Build** | March – April 2026 | Core application development |
| **Phase 3: Test & Recruit** | May – June 2026 | System testing, MN pilot customer acquisition |
| **Phase 4: Launch Prep** | Late June – July 7, 2026 | Final preparations, training, go-live readiness |

---

## Team & Roles

| Role                              | Person            | Responsibilities                                                          | Weekly Time Commitment |
| --------------------------------- | ----------------- | ------------------------------------------------------------------------- | ---------------------- |
| **Project Lead / Technical Lead** | Hamel Mesfin      | Overall project management, application development, infrastructure       | 25-30 hours            |
| **Clinical Lead**                 | Yonatan Berhe     | Knowledge extraction, PA criteria, clinical validation, reviewer training | 10-15 hours            |
| **Clinical Advisor**              | [Physician - TBD] | Clinical guidance, pilot customer intros, credibility                     | 2-3 hours              |
| **Legal/Admin**                   | Hamel Mesfin      | Contracts, BAAs, business formation                                       | As needed              |

---

## Phase 1: Foundation

### Timeline: January 1 – February 28, 2026

### Objectives

- Capture PA criteria knowledge for initial drug/PBM combinations
- Establish business and legal foundation
- Set up technical infrastructure
- Align team on roles, equity, and commitments
- Complete CMS data analysis to inform drug/payer targeting

---

### Workstream 1.1: Business Formation & Legal

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 1.1.1 | Decide on business entity structure (LLC vs C-Corp) | Project Lead | None | Jan 14 | ☐ Not Started |
| 1.1.2 | Register business entity | Project Lead | 1.1.1 | Jan 28 | ☐ Not Started |
| 1.1.3 | Obtain EIN from IRS | Project Lead | 1.1.2 | Jan 31 | ☐ Not Started |
| 1.1.4 | Draft founder/partner operating agreement | Project Lead | 1.1.1 | Feb 7 | ☐ Not Started |
| 1.1.5 | Review and sign operating agreement | All Partners | 1.1.4 | Feb 14 | ☐ Not Started |
| 1.1.6 | Set up business bank account | Project Lead | 1.1.2, 1.1.3 | Feb 14 | ☐ Not Started |
| 1.1.7 | Draft standard BAA template for customers | Project Lead | None | Feb 14 | ☐ Not Started |
| 1.1.8 | Draft pilot customer agreement template | Project Lead | None | Feb 21 | ☐ Not Started |
| 1.1.9 | Consult with healthcare attorney (if needed) | Project Lead | None | Feb 28 | ☐ Not Started |

**Deliverables:**

- [ ] Registered business entity
- [ ] Signed operating agreement
- [ ] BAA template
- [ ] Pilot agreement template

---

### Workstream 1.2: Knowledge Extraction

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 1.2.1 | Finalize initial drug list using CMS PA burden analysis (top 15) | Clinical Lead | None | Jan 14 | ☐ Not Started |
| 1.2.2 | Finalize initial PBM list (4 PBMs) using payer restrictiveness data | Clinical Lead | None | Jan 14 | ☐ Not Started |
| 1.2.3 | Gather official PA criteria documents from PBM websites | Clinical Lead | 1.2.1, 1.2.2 | Jan 21 | ☐ Not Started |
| 1.2.4 | Schedule knowledge extraction sessions | Project Lead | 1.2.3 | Jan 17 | ☐ Not Started |
| 1.2.5 | Complete extraction: Semaglutide (Ozempic/Wegovy) + Prime | Clinical Lead | 1.2.3 | Jan 28 | ☐ Not Started |
| 1.2.6 | Complete extraction: Semaglutide + Express Scripts | Clinical Lead | 1.2.5 | Feb 4 | ☐ Not Started |
| 1.2.7 | Complete extraction: Semaglutide + CVS Caremark | Clinical Lead | 1.2.6 | Feb 7 | ☐ Not Started |
| 1.2.8 | Complete extraction: Semaglutide + OptumRx | Clinical Lead | 1.2.7 | Feb 11 | ☐ Not Started |
| 1.2.9 | Complete extraction: Tirzepatide (Mounjaro) (all 4 PBMs) | Clinical Lead | 1.2.8 | Feb 18 | ☐ Not Started |
| 1.2.10 | Complete extraction: Adalimumab (Humira) (all 4 PBMs) | Clinical Lead | 1.2.9 | Feb 21 | ☐ Not Started |
| 1.2.11 | Complete extraction: Drugs #4-5 (Dulaglutide, Evolocumab) priority PBMs | Clinical Lead | 1.2.10 | Feb 25 | ☐ Not Started |
| 1.2.12 | Review and validate all extraction documents | Project Lead | 1.2.11 | Feb 28 | ☐ Not Started |

**Deliverables:**

- [ ] Data-driven prioritized drug list (CMS PA burden analysis)
- [ ] Prioritized PBM list with restrictiveness scoring
- [ ] 15-20 completed extraction worksheets (drug + PBM combinations)
- [ ] Source documentation library (official PA policies, forms)

---

### Workstream 1.3: Infrastructure Setup

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 1.3.1 | Register domain (firstpassrx.com) | Project Lead | None | Jan 7 | ☐ Not Started |
| 1.3.2 | Set up email (e.g., Google Workspace) | Project Lead | 1.3.1 | Jan 14 | ☐ Not Started |
| 1.3.3 | Provision server (Hetzner) | Project Lead | None | Jan 14 | ☐ Not Started |
| 1.3.4 | Configure Docker environment | Project Lead | 1.3.3 | Jan 21 | ☐ Not Started |
| 1.3.5 | Set up PostgreSQL database | Project Lead | 1.3.4 | Jan 21 | ☐ Not Started |
| 1.3.6 | Set up S3-compatible storage (Minio or Hetzner) | Project Lead | 1.3.4 | Jan 21 | ☐ Not Started |
| 1.3.7 | Configure SSL/TLS certificates | Project Lead | 1.3.1, 1.3.4 | Jan 28 | ☐ Not Started |
| 1.3.8 | Set up Git repository | Project Lead | None | Jan 7 | ☐ Not Started |
| 1.3.9 | Configure CI/CD pipeline (basic) | Project Lead | 1.3.8, 1.3.4 | Feb 7 | ☐ Not Started |
| 1.3.10 | Set up monitoring (Prometheus/Grafana or similar) | Project Lead | 1.3.4 | Feb 14 | ☐ Not Started |
| 1.3.11 | Configure backup strategy for database | Project Lead | 1.3.5 | Feb 14 | ☐ Not Started |
| 1.3.12 | Document infrastructure setup | Project Lead | 1.3.1-1.3.11 | Feb 21 | ☐ Not Started |

**Deliverables:**

- [ ] Production-ready server environment
- [ ] Database configured with backups
- [ ] File storage configured
- [ ] CI/CD pipeline operational
- [ ] Infrastructure documentation

---

### Workstream 1.4: Team Alignment

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 1.4.1 | Kickoff meeting with all partners | Project Lead | None | Jan 7 | ☐ Not Started |
| 1.4.2 | Align on equity/compensation structure | All Partners | 1.4.1 | Jan 21 | ☐ Not Started |
| 1.4.3 | Align on time commitments and responsibilities | All Partners | 1.4.1 | Jan 21 | ☐ Not Started |
| 1.4.4 | Identify potential clinical advisor candidates | All Partners | 1.4.1 | Jan 28 | ☐ Not Started |
| 1.4.5 | Reach out to clinical advisor candidates | Project Lead | 1.4.4 | Feb 7 | ☐ Not Started |
| 1.4.6 | Confirm clinical advisor (or continue search) | Project Lead | 1.4.5 | Feb 28 | ☐ Not Started |
| 1.4.7 | Establish regular meeting cadence | Project Lead | 1.4.1 | Jan 14 | ☐ Not Started |
| 1.4.8 | Set up project communication tools (Slack, etc.) | Project Lead | None | Jan 14 | ☐ Not Started |

**Deliverables:**

- [ ] Documented equity/compensation agreement
- [ ] Defined roles and responsibilities
- [ ] Clinical advisor identified (or pipeline established)
- [ ] Communication channels established
- [ ] Regular meeting schedule set

---

### Workstream 1.5: Market Analysis & Targeting

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 1.5.1 | Complete CMS Formulary PUF analysis (PA rates by drug/plan) | Project Lead | None | Jan 21 | ☐ Not Started |
| 1.5.2 | Complete Part D Prescribers dataset analysis (prescriber volume) | Project Lead | 1.5.1 | Jan 28 | ☐ Not Started |
| 1.5.3 | Analyze MN market opportunity (plans, prescribers, PA-gated cost) | Project Lead | 1.5.2 | Feb 7 | ☐ Not Started |
| 1.5.4 | Build PA burden scoring model for drug prioritization | Project Lead | 1.5.1 | Feb 7 | ☐ Not Started |
| 1.5.5 | Identify target payer list with restrictiveness rankings | Project Lead | 1.5.1 | Feb 14 | ☐ Not Started |
| 1.5.6 | Build value proposition model (market penetration × approval improvement) | Project Lead | 1.5.1, 1.5.2 | Feb 14 | ☐ Not Started |
| 1.5.7 | Document findings and update business plan | Project Lead | 1.5.1-1.5.6 | Feb 21 | ☐ Not Started |

**Deliverables:**

- [ ] Priority drug list ranked by PA burden score
- [ ] Target payer list with restrictiveness scores
- [ ] Value proposition model with scenario analysis
- [ ] MN market opportunity analysis
- [ ] Updated business plan with CMS data-backed metrics

---

### Phase 1 Milestone Checklist

**Target Date: February 28, 2026**

| Milestone | Status |
|-----------|--------|
| ☐ Business entity registered and operational | |
| ☐ Operating agreement signed by all partners | |
| ☐ 15-20 drug/PBM extraction worksheets completed | |
| ☐ Infrastructure environment ready for development | |
| ☐ Team aligned on roles, equity, and commitments | |
| ☐ Clinical advisor identified or in active discussions | |
| ☐ Legal templates (BAA, pilot agreement) drafted | |
| ☐ CMS data analysis complete with drug/payer targeting | |

---

## Phase 2: Build

### Timeline: March 1 – April 30, 2026

### Objectives

- Build core application (Django backend + Vue.js frontend)
- Implement validation engine with captured criteria
- Create reviewer workbench for PA processing
- Seed database with drug/PBM/criteria data

---

### Workstream 2.1: Backend Development (Django/DRF)

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 2.1.1 | Initialize Django project with standard structure | Project Lead | Phase 1 complete | Mar 5 | ☐ Not Started |
| 2.1.2 | Create core data models (Drug, PBM, PACriteria) | Project Lead | 2.1.1 | Mar 10 | ☐ Not Started |
| 2.1.3 | Create customer/practice models | Project Lead | 2.1.1 | Mar 10 | ☐ Not Started |
| 2.1.4 | Create PASubmission and related models | Project Lead | 2.1.2, 2.1.3 | Mar 14 | ☐ Not Started |
| 2.1.5 | Create document/attachment models | Project Lead | 2.1.4 | Mar 17 | ☐ Not Started |
| 2.1.6 | Implement DRF serializers for all models | Project Lead | 2.1.2-2.1.5 | Mar 21 | ☐ Not Started |
| 2.1.7 | Implement CRUD API endpoints | Project Lead | 2.1.6 | Mar 28 | ☐ Not Started |
| 2.1.8 | Implement file upload/download endpoints | Project Lead | 2.1.5, 2.1.7 | Mar 31 | ☐ Not Started |
| 2.1.9 | Implement authentication (Django auth or JWT) | Project Lead | 2.1.7 | Apr 4 | ☐ Not Started |
| 2.1.10 | Implement basic permissions/authorization | Project Lead | 2.1.9 | Apr 7 | ☐ Not Started |
| 2.1.11 | Write unit tests for models | Project Lead | 2.1.2-2.1.5 | Apr 11 | ☐ Not Started |
| 2.1.12 | Write unit tests for API endpoints | Project Lead | 2.1.7-2.1.8 | Apr 14 | ☐ Not Started |

**Deliverables:**

- [ ] Complete data model layer
- [ ] RESTful API for all core operations
- [ ] File upload/download functionality
- [ ] Authentication and basic authorization
- [ ] Unit test coverage for critical paths

---

### Workstream 2.2: Validation Engine

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 2.2.1 | Design validation engine architecture | Project Lead | 2.1.2 | Mar 14 | ☐ Not Started |
| 2.2.2 | Implement base PAValidator class | Project Lead | 2.2.1 | Mar 17 | ☐ Not Started |
| 2.2.3 | Implement required fields validation | Project Lead | 2.2.2 | Mar 21 | ☐ Not Started |
| 2.2.4 | Implement required documents validation | Project Lead | 2.2.2 | Mar 21 | ☐ Not Started |
| 2.2.5 | Implement step therapy validation | Project Lead | 2.2.2 | Mar 28 | ☐ Not Started |
| 2.2.6 | Implement lab requirements validation | Project Lead | 2.2.2 | Mar 28 | ☐ Not Started |
| 2.2.7 | Implement diagnosis code validation | Project Lead | 2.2.2 | Mar 31 | ☐ Not Started |
| 2.2.8 | Implement drug-specific validation rules (GLP-1s: Semaglutide, Tirzepatide, Dulaglutide) | Project Lead | 2.2.3-2.2.7 | Apr 7 | ☐ Not Started |
| 2.2.9 | Implement drug-specific validation rules (Oncology: Lenalidomide, Ibrutinib, Palbociclib) | Project Lead | 2.2.8 | Apr 11 | ☐ Not Started |
| 2.2.10 | Implement drug-specific validation rules (Immunology: Adalimumab, Etanercept, Dupilumab) | Project Lead | 2.2.9 | Apr 14 | ☐ Not Started |
| 2.2.11 | Implement validation result scoring | Project Lead | 2.2.3-2.2.7 | Apr 14 | ☐ Not Started |
| 2.2.12 | Implement recommendation generation | Project Lead | 2.2.11 | Apr 18 | ☐ Not Started |
| 2.2.13 | Create validation API endpoint | Project Lead | 2.2.2-2.2.12 | Apr 21 | ☐ Not Started |
| 2.2.14 | Write comprehensive tests for validation engine | Project Lead | 2.2.13 | Apr 25 | ☐ Not Started |
| 2.2.15 | Clinical review of validation logic | Clinical Lead | 2.2.14 | Apr 30 | ☐ Not Started |

**Deliverables:**

- [ ] Validation engine with PBM-specific rules
- [ ] Drug-specific validation for initial drug list (top 15 by CMS PA burden)
- [ ] Scoring and recommendation system
- [ ] Clinical sign-off on validation logic

---

### Workstream 2.3: Frontend Development (Vue.js)

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 2.3.1 | Initialize Vue.js project with standard structure | Project Lead | 2.1.7 | Mar 28 | ☐ Not Started |
| 2.3.2 | Set up API client and authentication | Project Lead | 2.3.1, 2.1.9 | Mar 31 | ☐ Not Started |
| 2.3.3 | Create login/authentication views | Project Lead | 2.3.2 | Apr 4 | ☐ Not Started |
| 2.3.4 | Create dashboard/home view | Project Lead | 2.3.3 | Apr 4 | ☐ Not Started |
| 2.3.5 | Create submission list view (queue) | Project Lead | 2.3.4 | Apr 7 | ☐ Not Started |
| 2.3.6 | Create submission detail view | Project Lead | 2.3.5 | Apr 11 | ☐ Not Started |
| 2.3.7 | Create submission form (new/edit) | Project Lead | 2.3.6 | Apr 14 | ☐ Not Started |
| 2.3.8 | Implement clinical data input components | Project Lead | 2.3.7 | Apr 18 | ☐ Not Started |
| 2.3.9 | Implement document upload component | Project Lead | 2.3.7, 2.1.8 | Apr 18 | ☐ Not Started |
| 2.3.10 | Implement validation results display | Project Lead | 2.3.6, 2.2.13 | Apr 21 | ☐ Not Started |
| 2.3.11 | Implement status workflow controls | Project Lead | 2.3.6 | Apr 25 | ☐ Not Started |
| 2.3.12 | Create basic reporting/metrics view | Project Lead | 2.3.4 | Apr 25 | ☐ Not Started |
| 2.3.13 | UI polish and responsiveness | Project Lead | 2.3.3-2.3.12 | Apr 30 | ☐ Not Started |

**Deliverables:**

- [ ] Functional reviewer workbench
- [ ] Submission management (create, view, edit)
- [ ] Document upload/viewing
- [ ] Validation results display
- [ ] Status workflow management
- [ ] Basic dashboard/metrics

---

### Workstream 2.4: Data Seeding

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 2.4.1 | Create data migration scripts for Drug model | Project Lead | 2.1.2, 1.2.12 | Mar 21 | ☐ Not Started |
| 2.4.2 | Create data migration scripts for PBM model | Project Lead | 2.1.2, 1.2.12 | Mar 21 | ☐ Not Started |
| 2.4.3 | Create data migration scripts for PACriteria | Project Lead | 2.1.2, 1.2.12 | Mar 28 | ☐ Not Started |
| 2.4.4 | Seed database with all extracted criteria | Project Lead | 2.4.1-2.4.3 | Apr 4 | ☐ Not Started |
| 2.4.5 | Validate seeded data against extraction worksheets | Clinical Lead | 2.4.4 | Apr 14 | ☐ Not Started |
| 2.4.6 | Create admin interface for criteria management | Project Lead | 2.4.4 | Apr 21 | ☐ Not Started |

**Deliverables:**

- [ ] Database populated with all drug/PBM/criteria data
- [ ] Admin interface for viewing/editing criteria
- [ ] Clinical validation of seeded data

---

### Phase 2 Milestone Checklist

**Target Date: April 30, 2026**

| Milestone | Status |
|-----------|--------|
| ☐ Django backend fully functional with all APIs | |
| ☐ Validation engine implemented and tested | |
| ☐ Vue.js reviewer workbench operational | |
| ☐ Database seeded with all extraction data | |
| ☐ End-to-end workflow functional (create → validate → submit) | |
| ☐ Clinical sign-off on validation logic | |

---

## Phase 3: Test & Recruit

### Timeline: May 1 – June 20, 2026

### Objectives

- Thoroughly test the system with realistic scenarios
- Identify and fix gaps in validation logic
- Sign 2-3 pilot customers from MN market
- Prepare operational processes and training

---

### Workstream 3.1: System Testing

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 3.1.1 | Create test case library (20-30 scenarios) | Clinical Lead | Phase 2 complete | May 7 | ☐ Not Started |
| 3.1.2 | Execute test cases - GLP-1 drugs (Semaglutide, Tirzepatide, Dulaglutide) | Clinical Lead | 3.1.1 | May 12 | ☐ Not Started |
| 3.1.3 | Execute test cases - Oncology drugs (Lenalidomide, Ibrutinib, Palbociclib) | Clinical Lead | 3.1.1 | May 16 | ☐ Not Started |
| 3.1.4 | Execute test cases - Immunology drugs (Adalimumab, Etanercept, Dupilumab) | Clinical Lead | 3.1.1 | May 19 | ☐ Not Started |
| 3.1.5 | Document validation gaps and issues | Clinical Lead | 3.1.2-3.1.4 | May 21 | ☐ Not Started |
| 3.1.6 | Fix identified validation issues | Project Lead | 3.1.5 | May 28 | ☐ Not Started |
| 3.1.7 | Re-test fixed issues | Clinical Lead | 3.1.6 | Jun 2 | ☐ Not Started |
| 3.1.8 | Test edge cases (denials, appeals, unusual scenarios) | Clinical Lead | 3.1.7 | Jun 6 | ☐ Not Started |
| 3.1.9 | Load test document uploads | Project Lead | Phase 2 complete | May 16 | ☐ Not Started |
| 3.1.10 | Security review (basic) | Project Lead | Phase 2 complete | May 23 | ☐ Not Started |
| 3.1.11 | Final system acceptance testing | Clinical Lead + Project Lead | 3.1.8 | Jun 13 | ☐ Not Started |

**Deliverables:**

- [ ] Test case library with expected results
- [ ] Test execution report
- [ ] All critical issues resolved
- [ ] System acceptance sign-off

---

### Workstream 3.2: Pilot Customer Acquisition (MN Market)

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 3.2.1 | Finalize target customer profile (MN endocrinology + rheumatology) | All Partners | None | May 5 | ☐ Not Started |
| 3.2.2 | Build prospect list (10-15 MN specialty practices) | All Partners | 3.2.1 | May 9 | ☐ Not Started |
| 3.2.3 | Prioritize prospects by likelihood and fit | All Partners | 3.2.2 | May 12 | ☐ Not Started |
| 3.2.4 | Customize pitch materials with CMS data (PA burden, MN market stats) | Project Lead | 3.2.3 | May 14 | ☐ Not Started |
| 3.2.5 | Begin outreach - Priority 1 prospects | All Partners | 3.2.4 | May 16 | ☐ Not Started |
| 3.2.6 | Conduct discovery calls | All Partners | 3.2.5 | May 16 – Jun 6 | ☐ Not Started |
| 3.2.7 | Deliver demos/presentations | Project Lead + Clinical Lead | 3.2.6 | May 23 – Jun 10 | ☐ Not Started |
| 3.2.8 | Negotiate pilot terms | Project Lead | 3.2.7 | May 30 – Jun 13 | ☐ Not Started |
| 3.2.9 | Execute pilot agreements | Project Lead | 3.2.8 | Jun 6 – Jun 20 | ☐ Not Started |
| 3.2.10 | Execute BAAs with pilot customers | Project Lead | 3.2.9 | Jun 6 – Jun 20 | ☐ Not Started |
| 3.2.11 | Begin outreach - Priority 2 prospects (if needed) | All Partners | 3.2.5 | May 23 | ☐ Not Started |

**Deliverables:**

- [ ] 2-3 signed pilot agreements (MN specialty practices)
- [ ] Executed BAAs with all pilot customers
- [ ] Clear understanding of each pilot's PA volume and drug mix

---

### Workstream 3.3: Operational Preparation

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 3.3.1 | Document intake process (how customers submit cases) | Project Lead | None | May 12 | ☐ Not Started |
| 3.3.2 | Document reviewer workflow (step-by-step) | Clinical Lead | Phase 2 complete | May 16 | ☐ Not Started |
| 3.3.3 | Create PBM submission guides (Prime, ESI, CVS, Optum) | Clinical Lead | None | May 23 | ☐ Not Started |
| 3.3.4 | Create submission templates/checklists per drug | Clinical Lead | 3.3.2 | May 30 | ☐ Not Started |
| 3.3.5 | Document escalation procedures (complex cases) | Clinical Lead | 3.3.2 | May 30 | ☐ Not Started |
| 3.3.6 | Document appeal/P2P procedures | Clinical Lead | None | Jun 2 | ☐ Not Started |
| 3.3.7 | Create customer onboarding checklist | Project Lead | 3.3.1 | Jun 2 | ☐ Not Started |
| 3.3.8 | Set up customer communication channels | Project Lead | 3.2.9 | Jun 13 | ☐ Not Started |
| 3.3.9 | Create FAQ document for customers | Project Lead | 3.3.1, 3.3.7 | Jun 13 | ☐ Not Started |

**Deliverables:**

- [ ] Intake process documentation
- [ ] Reviewer workflow documentation
- [ ] PBM submission guides (one per PBM)
- [ ] Customer onboarding checklist
- [ ] Escalation and appeal procedures

---

### Workstream 3.4: Training

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 3.4.1 | Develop reviewer training curriculum | Clinical Lead | 3.3.2 | May 30 | ☐ Not Started |
| 3.4.2 | Create training materials (slides, guides) | Clinical Lead | 3.4.1 | Jun 6 | ☐ Not Started |
| 3.4.3 | Conduct system training (tool usage) | Project Lead | 3.4.2 | Jun 10 | ☐ Not Started |
| 3.4.4 | Conduct clinical training (PA review process) | Clinical Lead | 3.4.2 | Jun 10 | ☐ Not Started |
| 3.4.5 | Practice with mock submissions | Clinical Lead | 3.4.3, 3.4.4 | Jun 16 | ☐ Not Started |
| 3.4.6 | Training sign-off (all reviewers ready) | Clinical Lead | 3.4.5 | Jun 20 | ☐ Not Started |

**Deliverables:**

- [ ] Reviewer training curriculum
- [ ] Training materials (slides, guides, videos)
- [ ] All reviewers trained and signed off

---

### Phase 3 Milestone Checklist

**Target Date: June 20, 2026**

| Milestone | Status |
|-----------|--------|
| ☐ System tested with 20-30 realistic scenarios | |
| ☐ All critical validation issues resolved | |
| ☐ 2-3 MN pilot customers signed with executed agreements | |
| ☐ BAAs in place with all pilot customers | |
| ☐ Operational processes documented | |
| ☐ All reviewers trained and ready | |

---

## Phase 4: Launch Preparation

### Timeline: June 21 – July 7, 2026

### Objectives

- Final go-live preparations
- Customer onboarding
- Launch readiness verification

---

### Workstream 4.1: Go-Live Readiness

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 4.1.1 | Final system verification | Project Lead | Phase 3 complete | Jun 23 | ☐ Not Started |
| 4.1.2 | Verify backup and recovery procedures | Project Lead | 4.1.1 | Jun 25 | ☐ Not Started |
| 4.1.3 | Verify monitoring and alerting | Project Lead | 4.1.1 | Jun 25 | ☐ Not Started |
| 4.1.4 | Create production user accounts | Project Lead | 4.1.1 | Jun 27 | ☐ Not Started |
| 4.1.5 | Go-live readiness checklist review | All Partners | 4.1.1-4.1.4 | Jun 30 | ☐ Not Started |
| 4.1.6 | Go/No-Go decision | All Partners | 4.1.5 | Jul 1 | ☐ Not Started |

**Deliverables:**

- [ ] Go-live readiness checklist complete
- [ ] Go/No-Go decision documented

---

### Workstream 4.2: Customer Onboarding

| ID | Task | Owner | Dependencies | Due Date | Status |
|----|------|-------|--------------|----------|--------|
| 4.2.1 | Onboarding call - Pilot Customer #1 | Project Lead + Clinical Lead | 3.2.9 | Jun 27-30 | ☐ Not Started |
| 4.2.2 | Onboarding call - Pilot Customer #2 | Project Lead + Clinical Lead | 3.2.9 | Jun 27-30 | ☐ Not Started |
| 4.2.3 | Onboarding call - Pilot Customer #3 | Project Lead + Clinical Lead | 3.2.9 | Jun 27-30 | ☐ Not Started |
| 4.2.4 | Share intake instructions with customers | Project Lead | 4.2.1-4.2.3 | Jul 2 | ☐ Not Started |
| 4.2.5 | Confirm customer readiness to submit cases | Project Lead | 4.2.4 | Jul 3 | ☐ Not Started |
| 4.2.6 | Set up customer check-in schedule | Project Lead | 4.2.5 | Jul 3 | ☐ Not Started |

**Deliverables:**

- [ ] All pilot customers onboarded
- [ ] Customers have intake instructions
- [ ] Check-in schedule established

---

### Phase 4 Milestone Checklist

**Target Date: July 7, 2026**

| Milestone | Status |
|-----------|--------|
| ☐ System verified and production-ready | |
| ☐ All pilot customers onboarded | |
| ☐ Team ready to receive first submissions | |
| ☐ Go/No-Go decision: GO | |

---

## Post-Launch: Pilot Operations (July 7 – September 30, 2026)

### Objectives

- Process real PA submissions
- Track outcomes and metrics
- Iterate based on learnings
- Build case studies for growth phase

---

### Weekly Pilot Operations Tasks

| Task | Owner | Frequency |
|------|-------|-----------|
| Review incoming submissions | Clinical Lead | Daily |
| Process and submit PAs to PBMs | Clinical Lead | Daily |
| Track submission outcomes | Project Lead | Daily |
| Customer check-ins | Project Lead | Weekly |
| Team sync meeting | All | Weekly |
| Metrics review | All | Weekly |
| Validation rule updates | Project Lead + Clinical Lead | As needed |
| System bug fixes | Project Lead | As needed |

### Pilot Success Metrics

| Metric | Target | Tracking Method |
|--------|--------|-----------------|
| First-pass approval rate | ≥85% | System tracking |
| Turnaround time (receipt → submission) | <24 hours | System tracking |
| Additional info request rate | <10% | System tracking |
| Customer satisfaction | High | Weekly check-ins |
| Validation accuracy | ≥95% | Clinical review |

### Pilot Milestone Schedule

| Date | Milestone |
|------|-----------|
| July 14 | Week 1 review - initial learnings |
| July 21 | Week 2 review - process adjustments |
| July 31 | Month 1 review - first metrics analysis |
| August 31 | Month 2 review - expanded customer onboarding |
| September 30 | Pilot complete - full results analysis |

---

## Risk Register

| Risk | Likelihood | Impact | Mitigation | Owner |
|------|------------|--------|------------|-------|
| Pharmacist partner availability constraints | Medium | High | Document knowledge early; cross-train if possible | Project Lead |
| Pilot customers don't engage or submit volume | Medium | High | Choose customers with acute pain; stay in close contact | All Partners |
| Validation rules have gaps or errors | Medium | Medium | Extensive testing; rapid iteration post-launch | Project Lead |
| PBM criteria change during pilot | Low | Medium | Monitor PBM policy updates; build update process | Clinical Lead |
| Technical issues delay development | Medium | Medium | Build buffer into schedule; prioritize MVP features | Project Lead |
| Legal/compliance issues discovered | Low | High | Consult healthcare attorney early; proper BAAs | Project Lead |
| Pilot customer acquisition takes longer than expected | Medium | Medium | Start outreach early; have backup prospects | All Partners |

---

## Communication Plan

### Internal Team

| Meeting | Frequency | Attendees | Purpose |
|---------|-----------|-----------|---------|
| Weekly Sync | Weekly (1 hour) | All Partners | Progress review, blockers, decisions |
| Daily Standup | Daily (15 min) | Project Lead + Clinical Lead | Quick status during build phase |
| Monthly Review | Monthly | All Partners | Strategic review, milestone assessment |

### Pilot Customers

| Communication | Frequency | Owner | Purpose |
|---------------|-----------|-------|---------|
| Onboarding Call | Once | Project Lead | Initial setup and training |
| Weekly Check-in | Weekly | Project Lead | Status, feedback, issues |
| Monthly Review | Monthly | Project Lead + Clinical Lead | Metrics, satisfaction, testimonials |

---

## Appendix A: Go-Live Readiness Checklist

### Technical Readiness

- [ ] All critical bugs resolved
- [ ] Performance acceptable under expected load
- [ ] Backup and recovery tested
- [ ] Monitoring and alerting configured
- [ ] SSL/security properly configured
- [ ] Production environment stable for 48+ hours

### Operational Readiness

- [ ] All processes documented
- [ ] All reviewers trained
- [ ] PBM submission access verified (portals, credentials)
- [ ] Escalation procedures defined
- [ ] Customer support process defined

### Customer Readiness

- [ ] All pilot agreements signed
- [ ] All BAAs executed
- [ ] All customers onboarded
- [ ] Intake instructions provided
- [ ] Customer contacts confirmed

### Business Readiness

- [ ] Invoicing/payment process defined
- [ ] Success metrics defined and tracking ready
- [ ] Communication templates ready
- [ ] Feedback collection process defined

---

## Appendix B: Key Contacts

| Role | Name | Email | Phone |
|------|------|-------|-------|
| Project Lead | | | |
| Clinical Lead | | | |
| Clinical Advisor | | | |
| Healthcare Attorney | | | |
| Pilot Customer #1 Contact | | | |
| Pilot Customer #2 Contact | | | |
| Pilot Customer #3 Contact | | | |

---

## Appendix C: Document Library

| Document | Location | Owner |
|----------|----------|-------|
| Extraction Worksheets | | Clinical Lead |
| Operating Agreement | | Project Lead |
| BAA Template | | Project Lead |
| Pilot Agreement Template | | Project Lead |
| Reviewer Training Materials | | Clinical Lead |
| PBM Submission Guides | | Clinical Lead |
| Customer Onboarding Checklist | | Project Lead |
| System Documentation | | Project Lead |
| CMS Data Analysis Deliverables | data_analysis/deliverables/ | Project Lead |

---

## Appendix D: CMS Data Analysis Key Findings

The following data from our CMS Formulary PUF and Part D Prescribers analysis informs our drug/payer targeting:

| Metric | Value | Implication |
|--------|-------|-------------|
| PA-gated annual drug spend | $75.5B | Large addressable market |
| Drugs with near-universal PA | 1,349 | Broad drug coverage opportunity |
| Annual MA PA requests | 52.8M | High volume = scalable business |
| Appeal overturn rate | 80.7% | Most denials are preventable with better submissions |
| Denials appealed | Only 12.2% | Massive gap = our value proposition |
| Recoverable approvals/year | 2.9M ($4.0B) | Quantifiable value we deliver |
| MN PA-gated cost | $1.06B | Strong pilot market |
| MN GLP-1 PA-gated cost | $247M | Validates endocrinology focus |
| Brand drug PA rate | 51.4% | Higher-cost drugs = higher PA burden |
| Drugs >$5K/claim PA rate | 85.7% | Specialty drugs are our sweet spot |

---

## Revision History

| Date | Version | Changes | Author |
|------|---------|---------|--------|
| | 1.0 | Initial document | |
| March 2026 | 2.0 | Updated go-live to July 7, 2026; integrated CMS data analysis; restructured phases | |

---

*This project plan is a living document and should be updated weekly during active execution.*
