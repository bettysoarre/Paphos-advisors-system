# Paphos Advisors — Claude Code Agent Guide

This file is loaded automatically when you open Claude Code in this repo.
It tells you which agent to activate and how.

---

## How to Activate an Agent

At the start of your session, tell Claude which agent you need:

> "Activate the Research Agent"
> "Activate the Brief Writer"
> "Activate the Content Writer"

Claude will read the relevant instruction file and operate as that agent for the session.

---

## The Three Content Pipeline Agents

### 1. Research Agent
**When to use:** You have a topic and need a sourced research package before writing begins.
**How it works:** The agent uses Perplexity to search and verify sources itself. You give it the topic — it does the research and outputs a structured package ready for the Brief Writer.
**Instruction file:** `paphos-advisor/prompts/agents/research-agent-instructions.md`
**Say:** "Activate the Research Agent. Topic: [your topic]. Target ICP: [ICP-00X]. Key questions to answer: [optional — list what you need to know]."

### 2. Content Brief Writer
**When to use:** The Research Agent has produced an approved research package and you need a complete content brief.
**How it works:** Paste the research package output from step 1. The agent converts it into a fully structured brief the Writer can execute without further input.
**Instruction file:** `paphos-advisor/prompts/agents/content-brief-writer-agent.md`
**Say:** "Activate the Brief Writer. Page: /[url-path]/. Research package: [paste research package]."

### 3. Content Writer
**When to use:** You have a human-approved brief and need a full draft.
**How it works:** Paste the approved brief. The agent drafts the full article from the brief and source material only — no searching, no filling from memory.
**Instruction file:** `paphos-advisor/prompts/agents/content-agent-instructions.md`
**Say:** "Activate the Content Writer. [Paste approved brief]."

---

## Pipeline Order

```
Research Agent → [human approves research] → Brief Writer → [human approves brief] → Content Writer → [human editorial review] → Publish
```

Never skip the human approval steps. A brief that has not been approved should not go to the Writer. A draft that has not been reviewed should not be published.

---

## Supporting Agents (Automated — No Manual Activation Needed)

| Agent | Trigger | What it does |
|---|---|---|
| Knowledge Lint Agent | Every Monday | Checks process docs for stale or conflicting information |
| Content Hygiene Agent | Every Friday | Checks Content Pipeline in Notion for overdue or missing fields |
| Blog Refresh Agent | Monthly (when live) | Updates published articles and adds "Latest update" box |

---

## Key Reference Files

| What you need | Where it is |
|---|---|
| Full agent registry and skills | `paphos-advisor/prompts/agents/_agent-skills-matrix.md` |
| Tone of voice rules | `paphos-advisor/content-system/style-guide/tone-and-voice.md` |
| Content brief template | `paphos-advisor/content-system/templates/content-brief-template.md` |
| ICP segment profiles | `paphos-advisor/icps/segments/` |
| ID registry (for new IDs) | `paphos-advisor/system/standards/id-registry.md` |
| All agent instruction files | `paphos-advisor/prompts/agents/` |
