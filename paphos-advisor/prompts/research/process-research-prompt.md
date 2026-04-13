---
id: PRMT-RES-001
title: "Process Research Prompt — Standard"
category: research
use_case: "Researching a new Cyprus process for documentation"
ai_system: perplexity
status: active
created: 2026-03-15
updated: 2026-04-13
related_sops:
  - SOP-RES-001
  - SOP-RES-002
  - SOP-RES-003
related_frameworks:
  - process-research-framework
tags:
  - prompt
  - research
  - process
---

# Process Research Prompt — Standard

## Purpose

Produces a comprehensive, structured research brief on a specific Cyprus administrative process — covering official requirements, eligibility, required documents, fees, office locations, processing times, step-by-step procedure, and known discrepancies between official guidance and real-world practice. The output is ready to be mapped directly into a process document using `process-template.md`.

---

## When to Use

Use when beginning research on a new Cyprus process for which no documentation yet exists in GitHub, or when revalidating an existing process document that may be out of date. This is the standard entry point for any new PROC-XXX document.

Do not use for quick fact-checks on a process you already have documented — use PRMT-RES-003 (Regulatory Update Check) for that.

---

## Inputs Required Before Running

Gather the following before executing this prompt:

- **Process name** — the full official name of the process (e.g. "EU National Residence Registration — MEU1 Application")
- **Domain / category** — immigration, tax, property, business, healthcare, transport, shipping, insurance, or settling-in
- **Target ICP segment(s)** — which ICP-SEG files this process applies to
- **Known official sources** — any government URLs you already have; paste them into the prompt if available
- **Whether an existing PROC-XXX file exists** — if updating rather than creating, note the current `confidence` and `status` values

**AI system:** Run in Perplexity using **Deep Research** mode for maximum source coverage. Sonar Pro or Sonar Deep Research are both suitable.

---

## The Prompt

```
[SYSTEM / CONTEXT]
You are a specialist researcher on Cypriot administrative and regulatory processes.
Your output will be used to create authoritative, accurate process documentation
for an advisory platform serving people relocating to Cyprus. Accuracy and source
attribution are critical — do not guess, do not generalise, and do not summarise
without citing a source.

[TASK]
Research the following process in detail:

Process: {PROCESS_NAME}
Applies to: {ICP_SEGMENTS — e.g. EU nationals relocating to Cyprus}
Category: {CATEGORY — immigration | tax | property | business | healthcare | transport | shipping | insurance | settling-in}

Research and answer each of the following sections in full.
Cite your sources inline using [Source: URL or document name] after every factual claim.

---

1. PROCESS OVERVIEW
Plain-language explanation of what this process is, why someone would need to do it,
and what the end result is. Write for a first-time relocator with no background in
Cypriot law or administration.

2. ELIGIBILITY
Who is eligible to use this process? Who is excluded? List all conditions including
nationality, residency status, income thresholds, age limits, or other qualifying criteria.
Note any edge cases or situations where eligibility is ambiguous.

3. REQUIRED DOCUMENTS
List every document required. For each document state:
- Document name
- Original, certified copy, or notarised copy?
- Apostille required? (yes / no / sometimes)
- Certified Greek translation required? (yes / no / sometimes)
- Any validity restriction (e.g. "issued within last 6 months")

4. FEES
List all fees at every stage. For each fee state:
- What it is for
- The exact amount in euros
- Who it is paid to (department or office)
- Accepted payment method (cash, bank transfer, JCC Smart portal, etc.)
- Date this fee was last confirmed or published

5. WHERE TO APPLY
- Name of the responsible government department or ministry
- Full address of the relevant office(s), by district where applicable
- Opening hours and appointment requirements
- Official online portal URL if digital submission is available
- Whether the applicant must attend in person or if a representative may attend

6. STEP-BY-STEP PROCEDURE
Complete numbered steps from start to finish. For each step include:
- What the applicant (or representative) must do
- Where they go or what they submit
- What the department does in response
- What the applicant receives at the end of that step
Be specific — name the department, form number, fee, and address.

7. PROCESSING TIME
- Official stated timeframe (as published by the relevant authority)
- Real-world timeframes reported by practitioners or applicants
- Factors that cause delays
- What the applicant receives on approval and in what form

8. RECENT CHANGES (last 24 months)
Any legislative, regulatory, or procedural changes in the last 24 months that affect
this process. Include the date of change and the source.

9. OFFICIAL SOURCES
List every official source used. For each:
- Full URL
- Page or document name
- Date accessed
- Government department or authority responsible

10. KNOWN DISCREPANCIES AND CONTRADICTIONS
Where official guidance contradicts real-world reports; where different official sources
conflict; where requirements vary by district, officer, or timing.
For each discrepancy: state the official position, the reported real-world situation,
and which is more likely accurate based on available sources.

11. CONFIDENCE ASSESSMENT
For each section above, assign: High / Medium / Low.
High — confirmed by official source and corroborated by practitioner reports.
Medium — credible secondary source or corroborated anecdotally but not officially confirmed.
Low — single source, anecdotal, or known to vary significantly by case.
List any sections where information is incomplete and further research is needed.

[CONSTRAINTS]
- Only cite official Cypriot government sources, EU law, or reputable legal/advisory publications
- Flag anything you are uncertain about with [UNCERTAIN]
- If information is unavailable from official sources, say so explicitly — do not fill gaps with assumptions
```

---

## Post-Processing Instructions

Once you have the Perplexity output:

1. **Run source validation** — check every cited URL is live and returns the correct page. Flag any dead links before proceeding (SOP-RES-002).

2. **Map to the process template** — use the output to populate a new PROC-XXX file following this mapping:

   | Research Section | Process Template Field |
   |-----------------|------------------------|
   | Process Overview | `## Overview` |
   | Eligibility | `## Eligibility` + `confidence` frontmatter |
   | Required Documents | `## Required Documents` |
   | Fees | `## Fees` |
   | Where to Apply | `## Where to Apply` |
   | Step-by-Step Procedure | `## Process Steps` |
   | Processing Time | `## Processing Time` |
   | Recent Changes | `## Recent Changes` + `last_validated` frontmatter |
   | Official Sources | `sources:` frontmatter array |
   | Known Discrepancies | `## Field Notes` + `## Common Issues` |
   | Confidence Assessment | `confidence:` + `source_type:` frontmatter |

3. **Set status to `in-research`** in the process file frontmatter. Do not mark as `review` until a human expert has checked the document.

4. **Save the raw research output** to the Research Log in Notion and reference it in the process file's `sources` frontmatter.

5. **Follow SOP-RES-001** (Research Capture) then **SOP-RES-003** (Knowledge Extraction) to extract KB articles from the research output.

---

## Known Limitations

- **URL hallucination** — Perplexity occasionally cites URLs that 404 or point to stale cached pages. Verify every source URL manually before using it in a process document.

- **Cypriot government site coverage** — several official Cypriot government portals (particularly CRMD, Civil Registry, and district-level offices) are poorly indexed. Perplexity may return incomplete results for these — supplement with direct portal checks.

- **Very recent changes (< 3 months)** — regulatory changes announced within the last 3 months may not yet appear in web search results. Always cross-check recent sections with the official ministry announcements page.

- **Local practice and officer discretion** — this prompt captures what is officially published. It cannot capture informal requirements, CRMD officer preferences, or district-level variations that exist only in practitioner knowledge. Supplement with field intelligence from the partner network and document findings as KA-FLD articles.

- **Non-English source material** — Greek-language official sources are often more current than their English translations. If the process area is heavily Greek-language, use Claude or GPT-4o with a translation step rather than Perplexity alone.

- **Complex multi-jurisdiction situations** — this prompt is designed for single-process research. It will produce shallow results for situations that require analysis across multiple legal systems (e.g. double tax treaty interactions). Use PRMT-ANL-001 for those cases.

---

## Changelog

| Date | Change | Author |
|------|--------|--------|
| 2026-04-13 | Restructured to PRMT schema; added post-processing mapping table, known limitations, related SOPs | lead-advisor |
| 2026-04-07 | Initial version | lead-advisor |
