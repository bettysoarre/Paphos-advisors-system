---
id: PRMT-CNT-002
title: FAQ Generation Prompt
type: content
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Structured FAQ page following faq-page-template.md
use_with: SOP-CON-001, content-system/content-types/faq-page.md
---

# FAQ Generation Prompt (PRMT-CNT-002)

## Purpose
Generate a structured FAQ page for a specific topic area based on the provided source material and question list.

## Tool
Claude

---

## Prompt

```
You are creating an FAQ page for Paphos Advisors, a Cyprus relocation advisory service. Your job is to write clear, direct, accurate FAQ content based on the source material and question list provided.

TOPIC: [TOPIC AREA — e.g., "Cyprus Yellow Slip (MEU1) for EU Nationals"]
TARGET ICP: [ICP SEGMENT]
TARGET KEYWORD: [PRIMARY KEYWORD — e.g., "yellow slip cyprus faq"]

QUESTIONS TO ANSWER:
[LIST THE QUESTIONS — one per line]

SOURCE MATERIAL:
[PASTE THE RELEVANT PROCESS DOC SECTIONS AND KB ARTICLES]

INSTRUCTIONS:
1. Answer each question directly in the first sentence — do not preamble
2. Keep each answer to 100-300 words maximum
3. Group questions by logical sub-topic (minimum 3 per group, maximum 12)
4. Name each group with a clear label (not a question)
5. Every factual claim must come from the source material — do not add facts not present
6. Where source material confidence is medium, add: "Note: This is based on practitioner experience. Verify with an official source before acting."
7. Write for the specific ICP — use language and assumptions appropriate to that segment
8. Include an FAQPage JSON-LD structured data block at the end covering all questions and answers
9. Write meta title and meta description at the top

FORMAT:
META TITLE: [50-60 chars]
META DESCRIPTION: [150-160 chars]

[Introduction — 1-2 sentences max]

## [Group 1 Label]

### [Question]
[Answer]

### [Question]
[Answer]

[Continue for all questions]

## Still have questions?
[Brief CTA]

[FAQPage JSON-LD block]
```

---

## How to Use

1. Prepare the question list from keyword research, case notes, or partner feedback
2. Paste the relevant source material
3. Run in Claude
4. Review answers against source material for accuracy
5. Proceed through SOP-CON-001
