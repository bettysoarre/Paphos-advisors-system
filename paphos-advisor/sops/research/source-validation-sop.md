---
id: SOP-RES-002
title: Source Validation SOP
area: research
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-RES-001, SOP-RES-003]
---

# Source Validation SOP

## Purpose
Defines how to assess whether a source is reliable enough to be cited in process documents or knowledge articles.

## Reference
Full validation checklist: `research/validation/source-validation-checklist.md`
Citation standards: `system/standards/source-citation-standards.md`

---

## Steps

### 1. Identify the source type
- **Official** — government website, legislation, official guidance document
- **Field** — partner interview, practitioner observation
- **Mixed** — combination of official and field, or secondary source citing official guidance

### 2. Apply the validation checklist
Work through `research/validation/source-validation-checklist.md`. Key questions:
- Is the source current? When was it last updated?
- Is the source authoritative for the claim being made?
- Does it apply to Cyprus (not another jurisdiction)?
- For official sources: is the URL from a `.gov.cy` or official registry domain?
- For field sources: is the source a regulated practitioner?

### 3. Cross-reference
Where possible, corroborate claims with at least one additional source:
- Official claim → cross-reference with legislation or a second official page
- Field claim → cross-reference with another practitioner or official source
- AI/research session output → always cross-reference with at least one official or field source

### 4. Assign confidence level
Based on validation outcome, assign a confidence level (from `system/taxonomies/confidence-levels.yaml`):
- **High** — official source confirmed, current, corroborated
- **Medium** — reliable source but not officially confirmed, or single field source
- **Low** — source has concerns (may be outdated, single uncorroborated field source)
- **Unverified** — not yet validated

### 5. Record in the source registry
If the source is a reusable official source, add it to `research/sources/official-sources-cyprus.md` if not already there.

### 6. Cite correctly
Follow `system/standards/source-citation-standards.md` when adding the citation to a process doc or KB article.

---

## When Sources Conflict
If two sources give different answers:
1. Prefer official sources over field sources for procedural facts
2. Prefer more recent sources over older ones
3. Note the conflict explicitly in the process doc `field_notes`
4. Do not silently choose one — flag the uncertainty with an appropriate confidence level
5. If the conflict is material, escalate to a partner for resolution before publishing
