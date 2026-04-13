---
id: RES-FRM-002
title: Regulatory Monitoring Framework
type: framework
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
applies_to: All Paphos Advisors process and knowledge documentation
linked_sops: [SOP-RES-003, SOP-RES-004]
---

# Regulatory Monitoring Framework (RES-FRM-002)

## Purpose
Defines how Paphos Advisors monitors for regulatory changes across the domains it operates in (immigration, tax, property, business) and how detected changes are processed into knowledge and content updates.

---

## Why This Matters

Cyprus regulatory information has a short shelf life:
- Tax rules change with each annual budget (typically October–November)
- Immigration circulars can change procedures without legislation
- Property transaction rules have changed multiple times in recent years
- EU policy changes flow into Cypriot law on irregular timescales

Without active monitoring, published content and process documents will diverge from reality — a material risk to client outcomes and business credibility.

---

## Monitoring Domains

### Domain 1 — Immigration

**What changes:** Permit types, eligibility criteria, required documents, processing times, fees, CRMD office procedures.

**Change frequency:** Medium. Most changes are via circular or administrative practice rather than legislation.

**Primary sources to monitor:**
- CRMD website — `crmd.moi.gov.cy` (announcements section)
- Ministry of Interior Cyprus — `moi.gov.cy`
- Official Gazette of Cyprus — for formal legislation
- EU Commission — for changes to Freedom of Movement rules

**Key trigger events:**
- Annual government budget (fees, thresholds)
- EU policy changes affecting third-country nationals
- Changes to Yellow Slip / MEU processing procedures
- Digital Nomad Visa — any extension or modification to the scheme

### Domain 2 — Tax

**What changes:** Tax rates, Non-Dom regime rules, GESY contributions, reporting deadlines, penalties.

**Change frequency:** High. Annual budget cycle; occasional mid-year amendments.

**Primary sources to monitor:**
- Cyprus Tax Department — `taxisnet.mof.gov.cy`
- Ministry of Finance announcements
- Official Gazette — for formal amendments
- ICPAC publications — for practitioner interpretation
- EU tax transparency directives — for corporate compliance

**Key trigger events:**
- Annual budget announcement (October/November)
- 60-Day Rule thresholds or conditions
- Non-Dom 17-year clock — any proposed changes
- GHS contribution rate changes
- IP Box scheme — any EU state aid review

### Domain 3 — Property

**What changes:** Transfer fees, stamp duty, title deed rules, mortgage legislation, land registry processes.

**Change frequency:** Medium. Major changes infrequent but impactful when they occur.

**Primary sources to monitor:**
- Department of Lands and Surveys — `dls.moi.gov.cy`
- Legal announcements from Ministry of Interior
- Cyprus Bar Association property law updates

**Key trigger events:**
- Transfer fee structure (stamp duty was abolished January 2026 — monitor for further changes)
- Title deed issuance — any government amnesty or accelerated scheme
- Immovable Property Tax — abolished 2017, but monitor for any reintroduction

### Domain 4 — Business Formation

**What changes:** Company registration requirements, accounting standards, substance rules, banking compliance.

**Change frequency:** Low–Medium. Changes driven by EU directives and OECD BEPS compliance.

**Primary sources to monitor:**
- Registrar of Companies — `efiling.drcor.mcit.gov.cy`
- ICPAC — for accounting and audit requirements
- OECD BEPS reports — for substance requirement changes
- Central Bank of Cyprus — for AML/KYC compliance affecting company banking

**Key trigger events:**
- Annual statutory filing deadlines
- EU Anti-Money Laundering Directive transposition
- OECD substance requirement updates affecting IP Box

---

## Monitoring Schedule

| Domain | Minimum Frequency | Trigger Review |
|---|---|---|
| Immigration | Monthly (passive scan) | Any CRMD circular or news report |
| Tax | Monthly (passive scan) + Annual deep review post-budget | Budget announcement / any Ministry press release |
| Property | Quarterly | Any DLS announcement or client case anomaly |
| Business | Quarterly | Any ICPAC bulletin or EU directive update |

**Passive scan** = 15-minute check of primary source websites for new announcements.  
**Deep review** = Run PROMPT-RES-003 (Regulatory Update Check) against affected process/knowledge documents.

---

## Change Detection Process

### Step 1 — Detect
A change is detected via one of:
- Scheduled monitoring scan
- Partner alert (partner reports a change during a referral interaction)
- Client case anomaly (something does not match our documented process)
- News or industry publication

### Step 2 — Classify
Classify the detected change:

| Type | Definition | Response |
|---|---|---|
| Confirmed change | Official source confirms new rule is in effect | Immediate revalidation — SOP-RES-004 |
| Proposed change | Legislation proposed but not enacted | Add note to affected docs; monitor |
| Rumoured change | Informal report, not confirmed | Flag for verification; do not update docs |
| Fee/time update only | Confirmed but minor (fee amount, wait time) | Update specific fields; no full revalidation |

### Step 3 — Impact Assessment
Identify what is affected:

1. Which process documents reference the changed rule?
2. Which KB articles cite the affected source?
3. Which published content pages include the outdated information?
4. Which active cases (if any) are affected?

### Step 4 — Update
Execute updates in this order:
1. Update the source knowledge (KB article)
2. Update process documents that reference it
3. Update any published content pages
4. Notify team of change (if it affects active cases)
5. Record in CHANGELOG

### Step 5 — Record
Log the change in the source registry with:
- Date change detected
- Date change took effect (if known)
- What changed
- What was updated in response
- Confidence level of the current position

---

## Emergency Monitoring Protocol

When a major change is detected (e.g., a rule affecting multiple active clients):

1. Flag immediately — do not wait for scheduled review
2. Add a warning note (`⚠ Rule under review — verify before advising`) to affected documents within 24 hours
3. Run full revalidation per SOP-RES-004 within 5 business days
4. Update published content within 5 business days of revalidation
5. If active cases are affected, escalate per SOP-CAS-003

---

## Monitoring Log

Changes detected are recorded in the Notion Research Log database with:
- Detection date
- Source of detection
- Domain affected
- Change classification
- Documents updated
- Status: open / resolved

---

## Integration with Annual Review

At the start of each calendar year:
1. Run a full scan of all Tier 1 process documents against current official sources
2. Run PROMPT-RES-003 for all domains
3. Update `next_review` dates in affected documents
4. Review the monitoring schedule — add any new sources identified
