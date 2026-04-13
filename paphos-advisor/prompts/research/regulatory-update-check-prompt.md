---
id: PROMPT-RES-003
title: Regulatory Update Check Prompt
type: research
tool: perplexity
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Change summary with dates, sources, and impact assessment
use_with: SOP-RES-004 (Process Revalidation SOP)
---

# Regulatory Update Check Prompt (PROMPT-RES-003)

## Purpose
Check whether a specific Cyprus process or regulation has changed since a given date. Use for scheduled process revalidation or when a change is suspected.

## Tool
Perplexity (Deep Research mode recommended)

---

## Prompt

```
I need to check whether there have been any changes to the following Cyprus process or regulation since [LAST REVIEW DATE]. This is for a Cyprus relocation advisory service and I need to ensure our documentation is current.

PROCESS/REGULATION: [PROCESS OR REGULATION NAME]

Please check:

1. REGULATORY CHANGES
- Have there been any legislative changes, amendments, or new regulations affecting this process since [LAST REVIEW DATE]?
- Provide the specific change, effective date, and source

2. PROCEDURAL CHANGES
- Have the practical procedures (forms, office requirements, processing times, fees) changed?
- Any announcements from the relevant government department?

3. PROPOSED CHANGES
- Are there any proposed changes currently in consultation or parliament?
- Any announced-but-not-yet-enacted changes?

4. CURRENT STATUS CONFIRMATION
Key facts I need to verify are still accurate:
[LIST THE SPECIFIC FACTS FROM THE EXISTING PROCESS DOC THAT NEED VERIFICATION]

5. SOURCE CONFIRMATION
- Are the official sources I should check still active? Official URLs: [LIST CURRENT URLS FROM PROCESS DOC]

Please provide citations for all claims.

PROCESS/REGULATION: [PROCESS OR REGULATION NAME]
LAST REVIEW DATE: [YYYY-MM-DD]
FACTS TO VERIFY: [LIST KEY FACTS]
OFFICIAL SOURCES TO CHECK: [LIST URLS]
```

---

## How to Use

1. Open the process doc to be revalidated
2. Fill in the process name, last review date, key facts from the process doc, and official source URLs
3. Run in Perplexity Deep Research
4. Save output to `assets/research-captures/revalidation-[process-slug]-[YYYY-MM-DD].md`
5. Update the process doc based on findings
6. Log in Research Log with type `Regulatory Update Check`
7. Update the process doc's `next_review_due` date

## Interpretation

**No changes found:** Update `updated` and `next_review_due` in the process doc frontmatter.
**Changes found:** Update all affected sections, update confidence level if appropriate, log in CHANGELOG if significant.
**Proposed changes pending:** Note in `field_notes` and set a shorter review cadence.
