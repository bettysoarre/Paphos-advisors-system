---
id: RES-VAL-001
title: Source Validation Checklist
type: validation-checklist
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
linked_sop: SOP-RES-002
---

# Source Validation Checklist (RES-VAL-001)

## Purpose
Step-by-step checklist for validating any source before it is cited in Paphos Advisors knowledge or content. Run this checklist per SOP-RES-002 for every new source before it is added to the source registry or cited in a document.

---

## Step 1 — Source Identity

- [ ] The source has a clearly identifiable publisher or author
- [ ] The publisher or author is named (not anonymous)
- [ ] The publication date is visible
- [ ] The URL or full document reference is available and accessible
- [ ] The source is the document itself, not a summary of the document by a third party

**If any of these fail:** The source cannot be cited. Find the primary source, or mark the claim as `confidence: unverified`.

---

## Step 2 — Authority Assessment

- [ ] Identify which authority tier applies (1, 2, or 3) using `research/sources/official-sources-cyprus.md` and `research/sources/third-party-sources.md`
- [ ] Confirm the publisher has jurisdiction over the topic (e.g., CRMD for immigration, Tax Department for tax)
- [ ] Confirm the source is specific to Cyprus (not a generic EU or international guide that may not apply)
- [ ] Check whether the source requires a professional licence to interpret correctly (e.g., legal opinion vs. official guidance)

**If Tier 3 or below:** This source requires corroboration from a Tier 1 or Tier 2 source before use.

---

## Step 3 — Currency Check

- [ ] The source publication date is known
- [ ] The source is within the acceptable freshness window for this content type:
  - Fees and thresholds: within 3 months
  - Processing times: within 3 months
  - Document checklists: within 6 months
  - Tax rates: within 12 months (or after most recent budget)
  - Eligibility criteria: within 12 months
  - Legislation references: within 12 months
- [ ] No subsequent legislation, circular, or amendment has been issued that supersedes this source
- [ ] If the source is outside the freshness window: add `⚠ Verify currency — sourced [date]` flag

---

## Step 4 — Relevance Check

- [ ] The source addresses the specific point being cited (not a related but different rule)
- [ ] The source applies to the correct applicant category (EU national vs. non-EU national rules are different)
- [ ] The source applies to the correct geography (Paphos-based applicants; CRMD offices differ)
- [ ] The source applies to the correct time period (pre-2020 Brexit transition rules are not current)

---

## Step 5 — Conflict Check

- [ ] Check whether other existing sources in the knowledge base address the same point
- [ ] If a conflict exists:
  - [ ] Document both positions
  - [ ] Determine which is more authoritative (Tier 1 beats Tier 2 beats Tier 3)
  - [ ] Determine which is more recent
  - [ ] Flag with: `[CONFLICT: Source A says X (date), Source B says Y (date) — resolve before use]`
  - [ ] Do not silently prefer one source

---

## Step 6 — Confidence Assignment

Based on the above:

| Result | Confidence level |
|---|---|
| Tier 1 source, within freshness window, no conflict | high |
| Tier 1 source, outside freshness window or minor conflict | medium |
| Tier 2 source, corroborated by Tier 1 | medium |
| Tier 2 source, not corroborated | low |
| Tier 3 source or field intelligence | low |
| Cannot confirm source accuracy | unverified |

- [ ] Confidence level assigned: ___________

---

## Step 7 — Registration

- [ ] Add the source to `research/sources/source-registry.csv` if not already listed
- [ ] Record: source_id, name, type, domain, URL, authority_tier, date validated, confidence_output, notes
- [ ] Cite the source in the document using the format from `system/standards/source-citation-standards.md`

---

## Common Failure Modes

| Issue | How to handle |
|---|---|
| Source is a blog post summarising official guidance | Find and cite the original official document |
| Source is undated | Cannot use — find dated equivalent or mark unverified |
| Source is in Greek only | Use with note: `[Translated from official Greek source — verify translation]` |
| Source contradicts partner intelligence | Document both; flag for partner verification |
| Source is a Perplexity answer | Treat as a lead only — validate each cited source individually |
| Source is from before 2020 | Check whether Brexit transition affects applicability |
