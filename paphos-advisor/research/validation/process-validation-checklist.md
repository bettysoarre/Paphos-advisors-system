---
id: RES-VAL-002
title: Process Validation Checklist
type: validation-checklist
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
linked_sop: SOP-RES-004
---

# Process Validation Checklist (RES-VAL-002)

## Purpose
Checklist for validating a process document before it advances to `validated` status or before it is used to inform client advice. Run this for new process documents and for scheduled revalidation per SOP-RES-004.

---

## Pre-Validation Setup

- [ ] Identify the process document being validated: ___________
- [ ] Note current status: stub / draft / in-research / review
- [ ] Note the last validation date (or `never` if new)
- [ ] Note the trigger for this validation: first validation / scheduled review / regulatory change / case anomaly

---

## Section 1 — Legal Basis

- [ ] The governing legislation or regulation is named
- [ ] The source for the legal basis is Tier 1 (Official Gazette, Ministry guidance, or CRMD)
- [ ] No more recent amendment has been issued that changes the legal basis
- [ ] EU directive basis (if applicable) is identified and still in force

**Confidence check:** If legal basis cannot be confirmed from primary source — process doc cannot advance to `validated`.

---

## Section 2 — Eligibility Criteria

- [ ] Applicant eligibility is clearly stated (nationality, residency status, income requirements, etc.)
- [ ] EU national and non-EU national paths are distinguished if applicable
- [ ] Income or asset thresholds are confirmed from a current official source (within 12 months)
- [ ] Age requirements (if any) are confirmed
- [ ] Exclusions or disqualifications are documented

**Flag:** `⚠ Verify thresholds — these change` added to any income/asset figures.

---

## Section 3 — Required Documents

- [ ] Document checklist sourced from official CRMD or authority guidance
- [ ] Each document's format requirements are noted (original / certified copy / apostille / translation)
- [ ] Document validity requirements are noted (e.g., bank statements not older than 3 months)
- [ ] Field intelligence reviewed for any practical additions to the official list
- [ ] Practical notes section updated with any divergence between official list and observed practice

---

## Section 4 — Fees

- [ ] Official fee amount confirmed from current source (within 3 months preferred; maximum 6 months)
- [ ] Payment method confirmed (bank transfer / cash / online portal)
- [ ] Any professional or notarial fees noted (clearly labelled as estimates, not official fees)
- [ ] Fee flagged with: `⚠ Fees change — verify current amounts before advising`

---

## Section 5 — Submission Process

- [ ] Submission location confirmed: in-person / postal / online portal
- [ ] Specific CRMD office for Paphos applicants confirmed
- [ ] Whether appointment is required confirmed
- [ ] Current appointment availability / wait times noted (from field intelligence, with date)
- [ ] What happens at the appointment is described

---

## Section 6 — Processing Times

- [ ] Official processing time sourced from CRMD or authority website
- [ ] Field intelligence processing time sourced from partner knowledge (with date)
- [ ] Both times documented: official and field-observed
- [ ] Processing time flagged with: `⚠ Processing times vary — verify current wait times with CRMD Paphos`

---

## Section 7 — Output and Validity

- [ ] Document or status issued is clearly described
- [ ] What the output permits is stated (what the client can do with it)
- [ ] Any conditions attached to the status are noted
- [ ] Validity period is confirmed from official source

---

## Section 8 — Renewal and Progression

- [ ] Renewal trigger (when must client act) is clearly stated
- [ ] Renewal process is described or cross-referenced to renewal process doc
- [ ] Pathway to next status level is noted (e.g., temporary → permanent residency)
- [ ] Automatic vs. application-required renewal distinction is clear

---

## Section 9 — Known Issues and Edge Cases

- [ ] Known rejection reasons documented (from field intelligence or official guidance)
- [ ] Office-specific variations noted (Paphos vs. Limassol vs. Nicosia)
- [ ] Recent changes noted with dates
- [ ] Open questions section completed (list any unresolved uncertainties)

---

## Section 10 — Document Quality

- [ ] Frontmatter complete: id, title, status, confidence, last_verified, next_review
- [ ] All sources cited with name, URL, date accessed
- [ ] Confidence level is consistent with source quality
- [ ] British English throughout
- [ ] No claims made without a source or explicit `[NEEDS SOURCE]` flag

---

## Validation Decision

After completing all sections:

| Outcome | Criteria |
|---|---|
| Advance to `validated` | All mandatory sections complete; no unresolved confidence conflicts; all high-change fields flagged |
| Return to `in-research` | Legal basis or eligibility sections incomplete; major gaps in required documents or fees |
| Escalate | Active client cases depend on this process and a significant change has been found |

- [ ] Decision: ___________
- [ ] Validated by: ___________
- [ ] Validation date: ___________
- [ ] Next review date: ___________ (12 months for Tier 1 processes; 6 months for high-change processes)

---

## Post-Validation Actions

- [ ] Update `status` in frontmatter to `validated`
- [ ] Update `last_verified` date in frontmatter
- [ ] Update `confidence` level in frontmatter if changed
- [ ] Set `next_review` date
- [ ] Update Notion Research Log record
- [ ] Check for downstream content pages that need updating — flag per SOP-RES-004
- [ ] Commit changes to GitHub
