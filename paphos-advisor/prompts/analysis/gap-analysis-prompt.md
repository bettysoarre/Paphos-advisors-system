---
id: PROMPT-ANA-001
title: Gap Analysis Prompt
type: analysis
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Scored gap list with priority recommendations
use_with: content-system/strategy/content-gap-analysis-framework.md
---

# Gap Analysis Prompt (PROMPT-ANA-001)

## Purpose
Analyse the current content library and knowledge base against our ICP needs and topical map to identify the highest-priority gaps.

## Tool
Claude

---

## Prompt

```
You are performing a content gap analysis for Paphos Advisors, a Cyprus relocation advisory service. Your job is to identify which content topics are missing or underserved, and prioritise them for production.

CURRENT CONTENT (what we have published):
[LIST TITLES AND URLS OF PUBLISHED CONTENT]

CONTENT IN PIPELINE (what we are producing):
[LIST TITLES OF IN-PRODUCTION CONTENT]

ICP PRIORITY ORDER:
1. EU National — Remote Worker
2. UK National — Retiree
3. Entrepreneur — Company Formation
4. Non-EU Digital Nomad
5. HNI — Permanent Residency
6. Family Relocating with Children

TOPICAL AREAS WE COVER:
1. Immigration & Residency
2. Tax & Financial Planning
3. Property
4. Business Formation
5. Healthcare
6. Settling In

ANALYSIS INSTRUCTIONS:
For each ICP segment and topical area combination:
1. Identify the 3-5 most searched questions/topics that we do not have content for
2. Score each gap on:
   - Demand (1-3): How frequently is this searched or asked?
   - ICP priority (1-3): How important is it for our priority ICP segments?
   - Revenue proximity (1-3): How close is this topic to the point of enquiry?
3. Flag whether we have the source material (validated process doc + KB articles) to write it now, or whether research is needed first

OUTPUT FORMAT:
For each gap, provide:
- Topic
- Content type recommended
- ICP segment(s) it serves
- Score (demand + ICP priority + revenue proximity = total/9)
- Source material ready? Yes / No — [what's missing if no]
- Priority: HIGH (7-9) / MEDIUM (4-6) / LOW (1-3)

End with a TOP 10 PRIORITY LIST sorted by score.
```
