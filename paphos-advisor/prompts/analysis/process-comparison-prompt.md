---
id: PROMPT-ANA-002
title: Process Comparison Prompt
type: analysis
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Structured comparison suitable for a comparison article
use_with: content-system/content-types/comparison-article.md
---

# Process Comparison Prompt (PROMPT-ANA-002)

## Purpose
Compare two or more Cyprus residency routes, tax structures, or property options based on process documentation, for use in a comparison article.

## Tool
Claude

---

## Prompt

```
You are creating a structured comparison for Paphos Advisors to use in a comparison article. Your job is to compare [OPTION A] and [OPTION B] across multiple dimensions using the process documentation provided.

COMPARISON: [OPTION A] vs [OPTION B]
PURPOSE: This comparison will be used in a content piece targeting [ICP SEGMENT]
KEY QUESTION THE READER IS TRYING TO ANSWER: [e.g., "Which residency route is right for me?"]

SOURCE MATERIAL — OPTION A:
[PASTE PROCESS DOC AND KB ARTICLES FOR OPTION A]

SOURCE MATERIAL — OPTION B:
[PASTE PROCESS DOC AND KB ARTICLES FOR OPTION B]

COMPARISON DIMENSIONS TO COVER:
[LIST THE DIMENSIONS — e.g., eligibility, cost, processing time, right to work, family inclusion, tax implications, ongoing requirements]

INSTRUCTIONS:
1. For each dimension, compare the two options factually based only on the source material
2. Use only facts present in the source material — do not add external knowledge
3. Where confidence of source material is medium, note this
4. Where the options are genuinely equal, say so — do not manufacture differences
5. Create:
   a. A quick comparison table (at-a-glance summary)
   b. A detailed side-by-side table covering all dimensions
   c. A "Choose [Option A] if..." / "Choose [Option B] if..." decision guide — be specific and direct
6. Flag any information gaps where the comparison cannot be made confidently

OUTPUT FORMAT:
QUICK COMPARISON TABLE
[Table]

DETAILED COMPARISON TABLE
[Table]

DECISION GUIDE
Choose [Option A] if:
- [Condition 1]
- [Condition 2]

Choose [Option B] if:
- [Condition 1]
- [Condition 2]

INFORMATION GAPS
[List any dimensions that could not be compared due to missing source material]
```
