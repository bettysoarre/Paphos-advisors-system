---
id: SOP-RES-001
title: Research Capture SOP
area: research
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-RES-002, SOP-RES-003]
---

# Research Capture SOP

## Purpose
Defines how to conduct and capture a research session so that the output is usable for knowledge extraction.

## When to Use
Before or during a Perplexity Deep Research session, an official source review, or any structured research activity.

---

## Steps

### 1. Define the research objective
Before starting, write down:
- What process or topic are you researching?
- What specific questions need to be answered?
- What will you do with the output? (Update a process doc? Create a new one? Validate an existing one?)

This prevents scope creep and ensures the output is usable.

### 2. Select the right prompt
Choose from `prompts/research/`:
- `process-research-prompt.md` (PROMPT-RES-001) — for researching a Cyprus administrative process
- `source-discovery-prompt.md` — for finding reliable sources on a topic
- `regulatory-update-check-prompt.md` — for checking if a process has changed recently
- `competitor-content-audit-prompt.md` — for content strategy research

### 3. Run the research session
For Perplexity:
- Use Deep Research mode
- Paste the prompt from the prompt library
- Fill in the [PROCESS NAME] and [SPECIFIC QUESTIONS] variables in the prompt
- Run the session

For official source review:
- Navigate to the relevant official sources (see `research/sources/official-sources-cyprus.md`)
- Screenshot or copy the relevant sections
- Note the URL and retrieval date

### 4. Export and save the output
Save the raw output to `assets/research-captures/`:
- Naming convention: `[topic-slug]-research-[YYYY-MM-DD].md`
- Example: `yellow-slip-meu1-research-2026-04-01.md`
- Include the date and tool used at the top of the file

### 5. Create a Research Log entry in Notion
Immediately after saving the capture file:
- Create a new entry in the Research Log
- Set status to `Captured`
- Record the capture file path
- Note the tool used and prompt used
- Note the initial confidence assessment

### 6. Flag open questions
Before closing the session, note any questions the research raised but did not resolve. Add these to the Research Log entry as `Open Questions`.

---

## Quality Standards
- Never skip saving the capture file. Raw outputs are the audit trail.
- Never extract knowledge from a session that was not captured first.
- If a session produces contradictory information, note the contradiction explicitly — do not just pick the version that fits.
