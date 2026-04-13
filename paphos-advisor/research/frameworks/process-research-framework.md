---
id: RES-FRM-001
title: Process Research Framework
type: framework
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
applies_to: All Cyprus administrative process documentation
linked_sops: [SOP-RES-001, SOP-RES-002, SOP-RES-003, SOP-RES-004]
---

# Process Research Framework (RES-FRM-001)

## Purpose
Defines how Paphos Advisors researches, validates, and maintains process documentation for Cyprus administrative procedures. Ensures every process document rests on authoritative sources and is kept current as rules change.

---

## What Is a Process?

For the purposes of this framework, a process is any defined administrative procedure that a client must follow to obtain a government document, permit, status, or registration in Cyprus.

Each process has:
- A defined applicant eligibility (who can apply)
- Required inputs (documents, fees, biometrics)
- A submission route (where and how to apply)
- An output (what is issued, what it means)
- A timeline (how long it takes at each stage)
- A validity period (how long the outcome lasts)
- Renewal or progression requirements (what comes next)

---

## Research Priority Tiers

Not all processes carry equal risk or complexity. Prioritise research depth accordingly.

### Tier 1 — High Priority (research to full depth)
Processes where errors cause significant client harm (visa refusal, overstay, tax penalty):

- Yellow Slip (MEU1) — EU nationals
- Category F Residency (financially independent)
- Digital Nomad Visa
- Non-Dom Tax Registration (60-Day Rule)
- Cyprus HE Company formation
- Category 6.2 Permanent Residency (investment)

### Tier 2 — Medium Priority (research key steps and gotchas)
Processes that are important but where errors are more easily corrected:

- Pink Slip (MEU3 — permanent residency EU nationals)
- ARC card application (third-country nationals in family unit)
- GESY registration
- Apostille and document legalisation
- Bank account opening (not a government process but client-critical)

### Tier 3 — Background Priority (research when needed)
Processes that arise less frequently or are well-documented elsewhere:

- VAT registration
- VIES registration
- Social insurance registration
- Municipal registration
- School enrolment (depends on school)

---

## Research Dimensions

For each process, research must cover all of the following dimensions. Gaps must be explicitly noted rather than omitted.

### 1. Legal Basis
- Which law or regulation governs this process?
- What EU directive (if any) is it derived from?
- Has there been recent legislation affecting it?

### 2. Competent Authority
- Which government department or office handles this?
- Which specific office handles Paphos applicants?
- Is there a distinction between first application and renewal?

### 3. Eligibility
- Who can apply? (nationality, residency status, employment status)
- Are there age requirements?
- Are there income/asset thresholds?
- Are there exclusions or disqualifications?

### 4. Required Documents
- What is the official document checklist?
- Are there variations depending on applicant circumstances?
- What format must documents be in? (original, certified copy, apostille, translation)
- What are the document validity requirements? (e.g., bank statements not older than 3 months)

### 5. Fees
- What are the official government fees?
- Are there additional professional or notarial fees typical for this process?
- How are fees paid? (bank transfer, cash, online)
- Note: `⚠ Fees change — verify current figures`

### 6. Submission
- Where is the application submitted? (in-person, post, online portal)
- Is an appointment required?
- What are the current appointment wait times?
- What happens at the appointment?

### 7. Processing Timeline
- What is the official processing time?
- What is the realistic current processing time (from field intelligence)?
- Are there expedition options?
- Note: `⚠ Processing times vary — verify with CRMD Paphos`

### 8. Output
- What document or status is issued?
- What does it permit?
- What are the conditions attached?
- What is the validity period?

### 9. Renewal and Progression
- When must the client renew?
- What does renewal require?
- What is the pathway to the next status (e.g., temporary → permanent residency)?

### 10. Known Issues and Edge Cases
- Common reasons for rejection or delay
- Known differences between offices (Paphos vs Limassol vs Nicosia)
- Partner-observed issues (field intelligence)
- Recent changes that have not yet propagated to official guidance

---

## Research Sources by Dimension

| Dimension | Primary Source | Secondary Source |
|---|---|---|
| Legal basis | Official Gazette of Cyprus | CRMD guidance documents |
| Competent authority | CRMD website | Partner knowledge |
| Eligibility | Official guidance | Immigration lawyer partner |
| Required documents | Official checklist | Partner knowledge (current practice) |
| Fees | Official fee schedule | Recent client case data |
| Submission | CRMD website | Partner knowledge |
| Processing timeline | CRMD website | Partner knowledge (field intelligence) |
| Output | Official guidance | Example documents (anonymised) |
| Renewal and progression | Official guidance | Immigration lawyer partner |
| Known issues | Field intelligence | Partner interviews |

---

## Research Session Cadence

| Trigger | Action |
|---|---|
| New process being documented for the first time | Full research across all 10 dimensions |
| Official notice of regulation change | Revalidation of affected dimensions — SOP-RES-004 |
| Partner reports change not reflected in our docs | Revalidation of affected dimensions |
| Scheduled review due (per process doc review date) | Targeted check on high-change dimensions (fees, timelines, document requirements) |
| Client case reveals discrepancy | Immediate spot-check — flag process doc for review |

---

## Output: Process Document Structure

Research outputs feed into process documents located in `processes/`. Each process document follows the template defined in `system/schemas/content-frontmatter-schema.yaml` and includes:

- Frontmatter with confidence level, last-verified date, next-review date
- All 10 research dimensions documented
- Open questions explicitly noted
- Source references at the bottom

See `knowledge/_templates/official-knowledge-template.md` for the article-level knowledge format.

---

## Quality Gate

A process document may not advance from `draft` to `validated` status unless:

- Legal basis confirmed from primary source
- Document checklist confirmed from official source
- At least one partner review of the field intelligence sections
- Fees and timelines marked with recency caveats
- Open questions section completed (even if empty: "No open questions identified")
