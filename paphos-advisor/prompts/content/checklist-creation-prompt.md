---
id: PROMPT-CON-003
title: Checklist Creation Prompt
type: content
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Structured checklist following checklist-template.md
use_with: SOP-CON-001, content-system/templates/checklist-template.md
---

# Checklist Creation Prompt (PROMPT-CON-003)

## Purpose
Create a practical, phase-structured checklist for a Cyprus process or relocation task based on source material.

## Tool
Claude

---

## Prompt

```
You are creating a checklist for Paphos Advisors, a Cyprus relocation advisory service. Your job is to create a practical, well-structured checklist that a client can actually use to complete [PROCESS/TASK].

CHECKLIST TOPIC: [PROCESS/TASK NAME]
TARGET ICP: [ICP SEGMENT]
RELATED PROCESS DOC: [PROC-XXX-NNN title]

SOURCE MATERIAL:
[PASTE THE RELEVANT PROCESS DOC AND KB ARTICLES]

INSTRUCTIONS:
1. Structure the checklist in logical phases with clear names and timing (e.g., "4-6 weeks before", "Week of appointment", "After submission")
2. Each task item format: ☐ [Action verb] [specific, concrete task] — [optional: where/how long/critical tip]
3. Tasks must be specific and actionable — no vague items like "prepare documents" (what documents, exactly?)
4. Include a Documents Required table with columns: Document | Format | Where to get it | Notes
5. Include a Timeline Summary table
6. Include a "Common Issues to Avoid" section (sourced from KB articles or process doc field notes)
7. Keep the language in second person (you/your), direct, and practical
8. Add the standard accuracy disclaimer at the end
9. Write meta title (50-60 chars) and meta description (150-160 chars)

FORMAT:
META TITLE: [50-60 chars — include "[Process] Checklist Cyprus"]
META DESCRIPTION: [150-160 chars]

[Intro — 2 sentences max]

## Before You Start
[Prerequisites]

## Phase 1: [Phase name]
[Tasks]

## Phase 2: [Phase name]
[Tasks]

### Documents Required
[Table]

## Timeline Summary
[Table]

## Common Issues to Avoid
[List]

## Next Steps
[Links]

[Disclaimer]
```

---

## How to Use

1. Identify the process to create a checklist for (must have a process doc at draft status or above)
2. Paste the relevant process doc as source material
3. Run in Claude
4. Review against the checklist content type definition
5. Proceed through SOP-CON-001
