---
id: PROMPT-CON-001
title: Guide Drafting Prompt
type: content
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Full draft following guide-page-template.md structure
use_with: SOP-CON-001, content-system/templates/guide-page-template.md
---

# Guide Drafting Prompt (PROMPT-CON-001)

## Purpose
Draft a relocation guide or process explainer based on the source material provided. Used by Claude to produce a draft that follows the guide page template.

## Tool
Claude

---

## Prompt

```
You are drafting content for Paphos Advisors, a Cyprus relocation advisory service. Your job is to write a well-structured, accurate, and practical guide based on the source material provided.

CONTENT BRIEF:
- Title: [TITLE]
- Content type: [relocation-guide / process-explainer]
- Target ICP: [ICP SEGMENT]
- Target keyword: [PRIMARY KEYWORD]
- Word count target: [WORD COUNT]
- Related process doc: [PROC-XXX-NNN title and key facts]

SOURCE MATERIAL:
[PASTE THE RELEVANT PROCESS DOC CONTENT AND KB ARTICLES HERE]

INSTRUCTIONS:
1. Follow the structure in the guide-page-template.md exactly:
   - H1, opening paragraph, required sections, FAQ section, next steps, disclaimer
2. Write in second person (you/your), present tense, active voice
3. Lead every section with the most important information — do not bury the key point
4. Every factual claim must come from the source material provided — do not add facts not present in the sources
5. Where source material has confidence: medium, add the enhanced accuracy disclaimer callout
6. Use the tone defined in tone-and-voice.md: knowledgeable, direct, honest — not promotional
7. Include the primary keyword naturally in the H1, opening paragraph, and at least 2 more times in the body
8. Write meta title (50-60 chars) and meta description (150-160 chars) at the top

OUTPUT FORMAT:
Start with:
META TITLE: [your meta title]
META DESCRIPTION: [your meta description]

Then the full article following the template structure.

Do not include anything not in the source material. If the source material has gaps, note them with [NEEDS SOURCE: what's missing] rather than inventing information.
```

---

## How to Use

1. Complete the content brief fields
2. Paste the relevant process doc sections and KB article excerpts as source material
3. Run in Claude
4. Review the draft against the content type definition and style guide
5. Proceed through SOP-CON-001 (Content Creation SOP)
