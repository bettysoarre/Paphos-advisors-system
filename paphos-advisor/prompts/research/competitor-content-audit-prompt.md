---
id: PROMPT-RES-004
title: Competitor Content Audit Prompt
type: research
tool: perplexity
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Structured analysis of competitor content for a topic area
use_with: content-system/strategy/content-gap-analysis-framework.md
---

# Competitor Content Audit Prompt (PROMPT-RES-004)

## Purpose
Analyse what competitors are publishing on a specific Cyprus relocation topic to identify content gaps, differentiators, and quality benchmarks. Used to inform content briefs.

## Tool
Perplexity (Deep Research mode)

---

## Prompt

```
I am planning content about [TOPIC] for a Cyprus relocation advisory website focused on Paphos. I need to understand what competitors are publishing and where the gaps are.

Please research the following:

1. TOP RANKING CONTENT
- What are the top 5-10 pieces of content currently ranking for searches about [TOPIC]?
- For each, provide: title, URL, publisher/website, approximate word count, and a brief description of what it covers

2. CONTENT QUALITY ASSESSMENT
For the top-ranking pieces:
- How accurate and up-to-date does the information appear?
- Are there obvious gaps, errors, or outdated information?
- What level of detail do they go into?
- Do they include practical/field intelligence or just official guidance?

3. SEARCH INTENT ANALYSIS
- What are the main questions people are asking about [TOPIC]?
- What information seems to be consistently missing from existing content?
- What formats are working (long guides, FAQs, checklists, comparisons)?

4. DIFFERENTIATION OPPORTUNITIES
- Where is there a clear gap that well-researched, field-validated content could fill?
- What angle would set new content apart from what already exists?
- Are there specific sub-topics that are underserved?

5. CONTENT FORMAT RECOMMENDATIONS
- Based on what is ranking, what format(s) would work best for new content on this topic?

TOPIC: [TOPIC]
Target audience: [ICP SEGMENT(S)]
Geographic focus: Paphos, Cyprus
```

---

## How to Use

1. Replace `[TOPIC]` with the specific topic (e.g., "Yellow Slip Cyprus EU national")
2. Replace `[ICP SEGMENT(S)]` with the target audience
3. Run in Perplexity
4. Save output to `assets/research-captures/competitor-audit-[topic-slug]-[YYYY-MM-DD].md`
5. Use findings to complete the Content Brief in Notion
6. Do not log as Research Log entry — this is a content planning tool, not a knowledge research session
