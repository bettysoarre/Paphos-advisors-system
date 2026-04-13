---
id: PROMPT-EXT-003
title: Research Session Extraction Prompt
type: extraction
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Structured KB article drafts from a Perplexity research session
use_with: SOP-RES-003 (Knowledge Extraction SOP)
---

# Research Session Extraction Prompt (PROMPT-EXT-003)

## Purpose
Extract structured knowledge from a Perplexity Deep Research session output and format it as KB article drafts. The research session output is treated as mixed confidence (official + synthesised) — not as primary source material.

## Tool
Claude

---

## Prompt

```
You are extracting structured knowledge from a Perplexity research session for the Paphos Advisors knowledge base. This research output is treated as mixed confidence — it synthesises multiple sources and has not been independently verified.

RESEARCH SESSION DATE: [YYYY-MM-DD]
PROMPT USED: [PROMPT-RES-001 / PROMPT-RES-002 / PROMPT-RES-003]
TOPIC: [Topic area]
CAPTURE FILE: [assets/research-captures/[filename]]

RESEARCH OUTPUT:
[PASTE THE PERPLEXITY OUTPUT HERE]

INSTRUCTIONS:
1. Read the research output and identify specific, actionable facts suitable for KB articles
2. Separate facts into:
   - LIKELY OFFICIAL (Perplexity cites a government source, or the fact is clearly a regulation/official requirement)
   - MIXED (synthesised from multiple sources, or Perplexity's own wording without a direct citation)
   - FIELD INTELLIGENCE (mentions of real-world practice that differs from official guidance)

3. For each extractable fact, create a KB article draft:

---
KB ARTICLE DRAFT
id: KB-[OFF/MXD/FLD]-[AUTO]
title: "[Specific claim]"
type: [official / field]
topic_area: [area]
confidence: [medium for official-sounding, low for mixed/synthesised]
source_type: [official / mixed]
source: "Perplexity Deep Research — PROMPT-RES-00X — [date] — Capture: [filename]"
related_process: [PROC-XXX-NNN if known]
validation_needed: [yes / no]

CLAIM:
[The specific factual claim]

SOURCE NOTE:
[What Perplexity cited for this claim, if anything. Note if no citation was given.]

VALIDATION REQUIRED:
[What needs to be verified against an official source or field partner]
---

4. Flag any claims that contradict our existing process docs with [CONFLICT: ...]
5. Flag any claims that seem implausible or inconsistent with what we know with [VERIFY URGENTLY: ...]
6. At the end: SUMMARY — total articles, number needing official validation, number needing field validation, key open questions the research raised

RESEARCH OUTPUT:
[PASTE HERE]
```

---

## Important Notes

- Research session extractions must be validated before being used in published content
- Set confidence to `medium` for facts that appear to be from official sources
- Set confidence to `low` for synthesised or uncited claims
- Never publish content citing only Perplexity as a source — trace back to the primary official source

## How to Use

1. Ensure the research capture file is saved in `assets/research-captures/`
2. Fill in session details and paste the research output
3. Run in Claude
4. Review extractions critically — Perplexity sometimes makes errors on procedural details
5. Create KB article files for validated extractions
6. Create follow-up research tasks for claims requiring validation
