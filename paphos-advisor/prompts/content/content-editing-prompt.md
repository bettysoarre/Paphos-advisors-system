---
id: PROMPT-CON-004
title: Content Editing Prompt
type: content
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Edited content with tracked changes and editorial notes
use_with: SOP-CON-002 (Content Review SOP)
---

# Content Editing Prompt (PROMPT-CON-004)

## Purpose
Edit a content draft for tone, clarity, structure, and compliance with editorial standards. Does NOT check factual accuracy — that is the reviewer's job.

## Tool
Claude

---

## Prompt

```
You are editing a content draft for Paphos Advisors, a Cyprus relocation advisory service. Your job is to improve tone, clarity, and structure — not to change facts or add new information.

CONTENT TYPE: [relocation-guide / process-explainer / faq-page / checklist / comparison-article]
TARGET ICP: [ICP SEGMENT]

EDITORIAL STANDARDS TO APPLY:
1. Tone: Knowledgeable, direct, honest. Not promotional, not overly cautious. Write like a trusted advisor who has been through the process themselves.
2. Voice: Second person (you/your), present tense, active voice
3. Clarity: Lead with the answer/key point. No preamble. Short sentences. One idea per paragraph.
4. Specificity: Replace vague language with specific facts. "Processing times vary" → "Processing typically takes 1-3 months at the Paphos CRMD office."
5. Headings: Should make sense out of context and be descriptive
6. British English spelling

THINGS TO FIX:
- Passive voice overuse
- Vague hedging ("may potentially", "could in some cases", "it is possible that")
- Preamble before the key point
- Paragraphs over 60 words
- Any "click here" anchor text
- Inconsistent formatting (numbered vs bullet lists, inconsistent heading levels)
- Promotional language ("our expert advisors", "we are the leading...")

THINGS NOT TO CHANGE:
- Factual claims (even if they seem unusual — they are sourced)
- Legal disclaimers
- Structured data/JSON-LD blocks
- Intentional notes like "[NEEDS SOURCE]" left by the author

DRAFT TO EDIT:
[PASTE DRAFT HERE]

Please provide the edited version. After the edited content, include a brief "Editorial Notes" section listing the main changes you made and why.
```

---

## How to Use

1. Use after a first draft has been created
2. Paste the full draft
3. Run in Claude
4. Review the editorial notes for any changes you disagree with
5. Use the edited version as the review draft in SOP-CON-002
