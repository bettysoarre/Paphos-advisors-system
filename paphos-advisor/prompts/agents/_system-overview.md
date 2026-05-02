---
id: PRMT-AGT-000
title: "Agent & Automation System Overview"
type: system-reference
version: "1.0"
created: 2026-05-01
updated: 2026-05-01
owner: lead-advisor
---

# Agent & Automation System Overview

Single-page navigator for the full Paphos Advisors automation system. For detail on any item, follow the links to the source file.

**Detailed references:**
- Full agent specs: [_agent-skills-matrix.md](_agent-skills-matrix.md)
- Full skill files: [../skills/](_index.md) (see `../skills/`)
- Session activation: [../../CLAUDE.md](../../CLAUDE.md)

---

## Scheduled Automations

Agents that run automatically without manual activation.

| Name | Schedule | Status | Output | Routine ID |
|---|---|---|---|---|
| Weekly Content Pipeline Hygiene | Every Friday 6am UTC | Active | Hygiene report in PA-Marketing and Branding (Notion) | trig_017VhqGhm6Uuj1GtwZjitLqp |
| Weekly Knowledge Lint (PRMT-AGT-004) | Every Monday 6am UTC | Active | Lint report committed to `paphos-advisor/research/lint-reports/` | trig_01V16x3BTyDvrwgGJVZbnqDw |
| Monthly Blog Refresh (PRMT-AGT-013) | Monthly — TBC | Not yet scheduled | Updated article files + diff summary | — |

Manage routines at: https://claude.ai/code/routines

---

## Agent Registry

| ID | Agent | Status | Phase | Skills | Purpose |
|---|---|---|---|---|---|
| PRMT-AGT-001 | Content Writer | Built | Live | SKL-WRI, SKL-TOV, SKL-SEO, SKL-GRD | Drafts website content from approved briefs |
| PRMT-AGT-002 | Research Agent | Built | Live | SKL-RES, SKL-GRD | Produces sourced research packages for content topics |
| PRMT-AGT-003 | Knowledge Ingest Agent | Built | Live | — | Processes new information into process docs and KB records |
| PRMT-AGT-004 | Knowledge Lint Agent | Built | Live (scheduled) | — | Weekly audit of process docs for stale/missing fields |
| PRMT-AGT-005 | Agent Skills Matrix | System ref | — | — | This document's source of truth |
| PRMT-AGT-006 | Content Brief Writer | Built | Live | SKL-BRF, SKL-SEO, SKL-TOV, SKL-GRD | Converts research packages into structured content briefs |
| PRMT-AGT-007 | Social Repurposing Agent | To build | Phase 1 | SKL-TOV, SKL-GRD, SKL-SOC-IG, SKL-SOC-FB, SKL-SOC-TK, SKL-SOC-X, SKL-SOC-LI | Atomises articles into per-platform social drafts |
| PRMT-AGT-008 | Instagram Social Agent | To build | Phase 2 | SKL-SOC-IG, SKL-TOV, SKL-GRD | Scheduled draft posts for Instagram |
| PRMT-AGT-009 | Facebook Social Agent | To build | Phase 2 | SKL-SOC-FB, SKL-TOV, SKL-GRD | Scheduled draft posts for Facebook |
| PRMT-AGT-010 | Community / Reactive Agent | To build | Phase 2 | SKL-COM, SKL-TOV, SKL-GRD | Monitors Reddit and Facebook groups; drafts response suggestions |
| PRMT-AGT-011 | PR / Link Research Agent | To build | Phase 3 | SKL-RES, SKL-PR, SKL-GRD | Identifies PR targets; drafts outreach pitches |
| PRMT-AGT-012 | Ads Analysis Agent | To build | Phase 3 | SKL-ADS, SKL-TOV, SKL-GRD | Competitor creative scan; draft ad copy suggestions |
| PRMT-AGT-013 | Monthly Blog Refresh Agent | To build | Phase 2 | SKL-RES, SKL-WRI, SKL-GRD | Monthly fact-check and update of published articles |
| PRMT-AGT-014 | Partner Knowledge Extraction Agent | To formalise | Phase 1 | SKL-EXT, SKL-GRD | Processes partner interview transcripts into KB records with risk classification |
| PRMT-AGT-015 | Chatbot Knowledge Agent | To build | Phase 2 | SKL-RAG, SKL-GRD, SKL-TOV | Customer-facing chatbot (chatbot.ai); answers from Safe to Use KB records only |

---

## Skills Library

| ID | Skill | Status | File | Assigned To |
|---|---|---|---|---|
| SKL-RES | Research with Citations | Built | [skl-res.md](../skills/skl-res.md) | AGT-002, AGT-011, AGT-013 |
| SKL-TOV | Tone of Voice | Built | [skl-tov.md](../skills/skl-tov.md) | AGT-001, AGT-006, AGT-007, AGT-013 |
| SKL-WRI | Writing Style | Built | [skl-wri.md](../skills/skl-wri.md) | AGT-001, AGT-013 |
| SKL-SEO | Formatting & SEO | Built | [skl-seo.md](../skills/skl-seo.md) | AGT-001, AGT-006 |
| SKL-GRD | Brand Guardrails | Built | [skl-grd.md](../skills/skl-grd.md) | All agents |
| SKL-BRF | Brief Writing | Built | [skl-brf.md](../skills/skl-brf.md) | AGT-006 |
| SKL-EXT | Knowledge Extraction | Built | [skl-ext.md](../skills/skl-ext.md) | AGT-014 |
| SKL-RAG | Chatbot / RAG Safety | Built | [skl-rag.md](../skills/skl-rag.md) | AGT-015 |
| SKL-SOC-IG | Social: Instagram | Pending — blocked on social guidelines (due 2026-05-05) | — | AGT-007, AGT-008 |
| SKL-SOC-FB | Social: Facebook | Pending — blocked on social guidelines (due 2026-05-05) | — | AGT-007, AGT-009 |
| SKL-SOC-TK | Social: TikTok | Pending — blocked on social guidelines (due 2026-05-05) | — | AGT-007 |
| SKL-SOC-X | Social: X/Twitter | Pending — blocked on social guidelines (due 2026-05-05) | — | AGT-007 |
| SKL-SOC-LI | Social: LinkedIn | Pending — blocked on social guidelines (due 2026-05-05) | — | AGT-007 |
| SKL-COM | Community Research | Pending — blocked on Gratian community playbook (due 2026-05-05) | — | AGT-010 |
| SKL-PR | PR Research & Pitch Drafting | Pending — Phase 3 | — | AGT-011 |
| SKL-ADS | Ads Analysis | Pending — Phase 3 | — | AGT-012 |

---

## Pipeline Map

### Content Pipeline
```
Topic request
  → Research Agent (AGT-002)         [HUMAN: approve research]
  → Brief Writer (AGT-006)           [HUMAN: approve brief]
  → Content Writer (AGT-001)         [HUMAN: editorial review]
  → Publish to GitHub + Notion
```

### Partner Knowledge Pipeline
```
Interview transcript (Google Drive)
  → Save to repo + Notion Interviews DB
  → Knowledge Extraction Agent (AGT-014)   [HUMAN: review Internal Only + Do Not Use records]
  → KB records available to Research Agent + Chatbot (AGT-015)
```

### Social Pipeline
```
Published article
  → Social Repurposing Agent (AGT-007)     [HUMAN: approve each platform draft]
  → Manual post via Canva + scheduler
  (Phase 2: Platform agents draft to queue → human approves → post)
```

### Content Refresh Pipeline
```
Monthly scheduled trigger
  → Blog Refresh Agent (AGT-013)           [HUMAN: review diff before committing]
  → Commit to GitHub → recrawl trigger
```

---

## Human Gates — Never Skip

| Gate | Agent | What the human decides |
|---|---|---|
| Research approval | AGT-002 | Research package is complete and reliable |
| Brief approval | AGT-006 | Angle, scope, and structure are correct |
| Content approval | AGT-001 | Content is accurate, on-brand, ready to publish |
| KB classification review | AGT-014 | Internal Only and Do Not Use records are correctly flagged |
| Social approval | AGT-007/008/009 | Post is accurate, appropriate, on-brand |
| Refresh approval | AGT-013 | Factual updates are correct and complete |
| PR outreach | AGT-011 | Pitch is appropriate — human sends, never the agent |

---

## Build Roadmap

| Phase | What | Blocker |
|---|---|---|
| Phase 1 — Now | Formalise AGT-014 (Knowledge Extraction) | Add Reuse Classification field to Notion KB |
| Phase 1 — Now | Build AGT-007 (Social Repurposing) | Canva templates needed |
| Phase 2 — May | Build social skills (SKL-SOC-*) and AGT-008/009 | Social guidelines from Gratian (due 2026-05-05) |
| Phase 2 — May | Build AGT-010 (Community) | Community playbook from Gratian (due 2026-05-05) |
| Phase 2 — May | Build AGT-013 (Blog Refresh) + schedule | Website live; GitHub–Notion sync in place |
| Phase 2 — May | Build AGT-015 (Chatbot) | chatbot.ai connected; KB Reuse Classification fully populated |
| Phase 3 — Jun+ | Build AGT-011 (PR) | Core content pipeline stable |
| Phase 3 — Jun+ | Build AGT-012 (Ads Analysis) | Campaign running; performance data available |
