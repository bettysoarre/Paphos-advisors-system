---
id: PROMPT-RES-001
title: Cyprus Process Research Prompt (Perplexity)
use_case: >
  Research a Cyprus administrative process using Perplexity. Produces a structured
  research output ready to populate a process document using process-template.md.
target_tool: Perplexity (sonar-pro or sonar-deep-research)
created: 2026-04-07
updated: 2026-04-07
tags:
  - research
  - immigration
  - tax
  - property
  - cyprus-wide
  - advisors
---

## Context

Use this prompt when you need to research a Cyprus administrative process from scratch or
update an existing process document. Run it in Perplexity using the **Deep Research** mode
for maximum source coverage.

Before running, you must know:
- The name of the process you are researching
- Which ICP segment(s) it applies to (from `icp-segments.yaml`)
- The process category (from `tag-registry.yaml` — process dimension)

After running, take the output and use it to populate or update the corresponding
`.md` process file using `process-template.md`.

---

## Objective

Produce a comprehensive, structured research brief on a specific Cyprus administrative
process — covering official requirements, fees, office locations, processing times,
eligibility, and any known discrepancies between official guidance and real-world practice.

---

## Instructions

Copy the prompt below, fill in all `[PLACEHOLDERS]`, and run it in Perplexity Deep Research.

---

```
You are a specialist researcher on Cypriot administrative and regulatory processes.
Your task is to produce a comprehensive, structured research brief on the following process:

**Process:** [FULL NAME OF THE PROCESS — e.g. "EU National Residence Registration (MEU1 Application)"]
**Applies to:** [ICP SEGMENTS — e.g. "EU nationals relocating to Cyprus"]
**Category:** [CATEGORY — e.g. immigration | tax | property | business | healthcare | transport | shipping | insurance | settling-in]

---

Research and answer each of the following sections in full. Cite your sources inline
using [Source: URL or document name] after every factual claim. Do not summarise or
paraphrase without attribution.

---

### 1. Process Overview
Provide a plain-language explanation of what this process is, why someone would need to
do it, and what the end result is. Write for someone relocating to Cyprus for the first
time who has no background in Cypriot law or administration.

### 2. Eligibility
Who is eligible to use this process? Who is excluded? List all conditions, including
nationality, residency status, income thresholds, age limits, or other qualifying criteria.
Note any edge cases or situations where eligibility is ambiguous.

### 3. Required Documents
List every document required for this process. For each document state:
- The document name
- Whether an original, certified copy, or notarised copy is required
- Whether an apostille is needed
- Whether a certified translation into Greek is required
- Any validity restrictions (e.g. "issued within the last 6 months")

Present as a numbered list.

### 4. Fees
List all fees at every stage of the process. For each fee state:
- What it is for (application fee, stamp duty, processing fee, etc.)
- The exact amount in euros
- Who it is paid to (which department or office)
- The accepted payment method (cash, bank transfer, tax payment portal, etc.)
- The date this fee information was last confirmed or published

Note any fees that vary by case type, nationality, or other factors.

### 5. Where to Apply
State exactly where this application is submitted. Include:
- The name of the responsible government department or ministry
- The full address of the relevant office(s), broken down by district where applicable
- Opening hours and appointment requirements
- The official online portal URL if applications can be submitted digitally
- Whether the applicant must attend in person or if a legal representative can attend

### 6. Process Steps
Provide a complete, numbered, step-by-step breakdown of the process from start to finish.
For each step include:
- What the applicant (or their representative) must do
- Where they go or what they submit
- What the department does in response
- What the applicant receives at the end of that step

Be specific. Do not use vague language like "submit the application". State what is
submitted, to whom, and how.

### 7. Processing Time
State the expected time from submission to final outcome. Include:
- The official stated timeframe (as published by the relevant authority)
- Any real-world timeframes reported by practitioners or applicants
- Factors that cause delays (peak periods, incomplete documents, officer discretion)
- What the applicant receives when approved and in what form (card, letter, stamp, etc.)

### 8. Official Sources
List every official source used in this research brief. For each:
- Full URL
- Name of the page or document
- Date accessed
- Government department or authority responsible for the source

### 9. Known Discrepancies and Contradictions
Document any cases where:
- Official guidance contradicts real-world reports from practitioners or applicants
- Different official sources give conflicting information
- The process described officially does not match what offices actually require in practice
- Requirements vary by district, officer, or timing

For each discrepancy, state the official position, the reported real-world situation,
and your assessment of which is more likely to be accurate based on the sources available.

### 10. Confidence Assessment
For the information in each section above, assign a confidence level:
- **High** — confirmed by official source and corroborated by practitioner reports
- **Medium** — from a credible secondary source or corroborated anecdotally but not officially confirmed
- **Low** — single source, anecdotal, or known to vary significantly by case

List any sections where the information is incomplete and further research is needed.
```

---

## Output Format

The Perplexity output should be a structured document with all 10 sections completed.
Once received, map the output to `process-template.md` as follows:

| Research Section | Process Template Field / Section |
|-----------------|----------------------------------|
| Process Overview | `## Overview` |
| Eligibility | `## Eligibility` + `status`, `confidence` frontmatter |
| Required Documents | `## Required Documents` |
| Fees | `## Fees` |
| Where to Apply | `## Where to Apply` |
| Process Steps | `## Process Steps` |
| Processing Time | `## Processing Time` |
| Official Sources | `sources:` frontmatter array |
| Known Discrepancies | `## Field Notes` + `## Common Issues` |
| Confidence Assessment | `confidence:` + `source_type:` frontmatter |

Set `status: in-research` in the frontmatter when saving the initial research output.
Upgrade to `review` only after a human expert has checked the document.

---

## Example Filled-In Prompt

Below is an example of the prompt filled in for a specific process.
Use this as a reference for how to complete the placeholders.

```
You are a specialist researcher on Cypriot administrative and regulatory processes.
Your task is to produce a comprehensive, structured research brief on the following process:

**Process:** EU National Residence Registration — MEU1 Application (Yellow Slip)
**Applies to:** EU nationals (non-Cypriot) relocating to Cyprus as their primary residence
**Category:** immigration

---

Research and answer each of the following sections in full. Cite your sources inline
using [Source: URL or document name] after every factual claim. Do not summarise or
paraphrase without attribution.

### 1. Process Overview
[Research the MEU1 registration process...]

### 2. Eligibility
[Who qualifies as an EU national for this process? What are the income/accommodation
requirements for different categories — worker, self-employed, student, self-sufficient?]

### 3. Required Documents
[List all documents required for an MEU1 application, including originals vs. copies,
apostille requirements, and translation requirements...]

[... continue all 10 sections ...]
```
