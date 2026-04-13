---
id: RES-VAL-003
title: Knowledge Accuracy Criteria
type: validation-criteria
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
linked_sops: [SOP-KNW-001, SOP-KNW-002]
---

# Knowledge Accuracy Criteria (RES-VAL-003)

## Purpose
Defines the accuracy standards that Paphos Advisors knowledge articles must meet at each lifecycle stage. Used by the knowledge review process (SOP-KNW-002) and by anyone assessing whether an article is fit for use in client-facing content or case work.

---

## Why Accuracy Criteria Matter

Knowledge articles in this system are used to:
1. Inform content written for the public website (accuracy errors become published misinformation)
2. Brief advisors handling client cases (accuracy errors become bad advice)
3. Train partner knowledge extraction (accuracy errors compound)

The cost of an error is higher than the cost of a gap. A clearly flagged gap (`[NEEDS SOURCE]`) is safe. An unflagged error is not.

---

## Criteria by Knowledge Article Type

### Official Knowledge Articles (KB-OFF-NNN)

Official knowledge articles document the regulatory and legal position from authoritative government or EU sources.

**Accuracy criteria:**

| Criterion | Requirement |
|---|---|
| Source attribution | Every claim must cite a specific Tier 1 source |
| Source currency | Source must be within the freshness window for its content type |
| Direct quotation | Key provisions must include a direct quote or close paraphrase with citation |
| Applicant scope | Article must specify who this applies to (nationality, residency status) |
| Effective date | Article must state when the rule came into force |
| Known limitations | Must note any known gaps in official guidance or pending changes |
| Confidence level | `high` only if source is Tier 1 and within freshness window |

**Disqualifying issues (article cannot be used until resolved):**
- Claim without a source citation
- Source outside freshness window without a currency flag
- Conflation of EU national and non-EU national rules
- Fee or threshold figures without a `⚠ Verify current amounts` note

---

### Field Knowledge Articles (KB-FLD-NNN)

Field knowledge articles document practitioner intelligence that supplements or diverges from official guidance.

**Accuracy criteria:**

| Criterion | Requirement |
|---|---|
| Source attribution | Must identify source tier (partner interview / case observation / community) |
| Corroboration | Must note whether the claim has been corroborated and by how many sources |
| Divergence note | Must state whether this confirms, supplements, or contradicts official guidance |
| Date of intelligence | Must state when the information was gathered, not just when the article was written |
| Confidence level | `low` unless corroborated by two or more independent Tier 1 field sources |

**Disqualifying issues:**
- Field claim presented without noting it is field intelligence (not official guidance)
- Unattributed claim presented as practitioner knowledge
- Claim that contradicts official guidance without explicitly flagging the divergence

---

### Decision Tree Articles (KB-DEC-NNN)

Decision trees are logic documents derived from process knowledge and eligibility criteria.

**Accuracy criteria:**

| Criterion | Requirement |
|---|---|
| Branching logic source | Each branch must reference the process doc or KB article it derives from |
| Completeness | All known eligibility dimensions covered; gaps explicitly noted |
| No advice | Decision trees guide enquiry — they must not constitute advice |
| Edge case documentation | Known exceptions or grey areas must be noted at relevant decision points |
| Disclaimer | Standard disclaimer must appear prominently |

**Disqualifying issues:**
- Branch based on assumption without a source
- Missing disclaimer
- Any branch that appears to tell the reader what they "should" do

---

## Confidence Level Definitions in Practice

### `confidence: high`
- Based on Tier 1 official source
- Verified within the freshness window
- No conflicting evidence from other Tier 1 sources
- Reviewed in the last 12 months

**Use in:** Any context — client case briefing, content drafting, partner knowledge base.

### `confidence: medium`
- Based on Tier 1 source but outside freshness window, **or**
- Based on Tier 2 source corroborated by Tier 1, **or**
- High confidence on the principle but uncertainty on specific figures (fees, timelines)

**Use in:** Content drafting with appropriate hedging language. Client case briefing with a verification note. Not as a standalone basis for advice on time-sensitive matters.

### `confidence: low`
- Based on field intelligence (practitioner or case observation)
- Not yet corroborated by official source
- Tier 3 source or community intelligence

**Use in:** Background context only. Must be explicitly labelled as field intelligence. Not for published content without hedging. Not as basis for advice without verification.

### `confidence: unverified`
- Cannot confirm the source
- Source conflicts with other evidence and conflict is unresolved
- Source is outside any acceptable freshness window

**Use in:** Log for investigation only. Must not appear in published content or be used to brief clients. Flag for immediate resolution.

---

## Red Flags During Review

The following should trigger an immediate accuracy review:

| Red flag | Why it matters |
|---|---|
| Fee or threshold figures without a date | Fees change; outdated figures cause client harm |
| Processing time stated as a definite figure | Times vary significantly; false precision misleads clients |
| "All applicants" or "always" language | Cyprus rules have many exceptions; absolutist claims are usually wrong |
| EU and non-EU nationals described the same way | These are different legal regimes with different processes |
| Pre-2020 sources cited for immigration rules | Brexit transition changed many things; old sources may be wrong |
| "Cyprus doesn't have..." statements | These are frequently wrong and high-risk if incorrect |
| Any claim not supported by a source citation | Even if probably correct, an uncited claim fails accuracy standards |

---

## Escalation

If a knowledge article is found to contain a material error (i.e., something that could directly lead to incorrect client advice):

1. Update status to `needs-revalidation` immediately
2. Add a `[SUSPENDED: material accuracy issue — do not use]` notice at the top of the article
3. Flag all content pages that cite this article
4. Fix the article per SOP-KNW-002 review process
5. If the error may have already been used in client advice, escalate per SOP-CAS-003
