---
id: PRMT-RES-002
title: Source Discovery Prompt
type: research
tool: perplexity
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Structured list of sources with URLs, authority level, and notes
use_with: SOP-RES-001, SOP-RES-002
---

# Source Discovery Prompt (PRMT-RES-002)

## Purpose
Find and catalogue reliable official sources for a specific Cyprus topic area. Use before or alongside a process research session to build the source registry.

## Tool
Perplexity (Standard or Deep Research mode)

---

## Prompt

```
I am building a reference library of official and authoritative sources for Cyprus administrative processes and regulations. I need to find reliable sources for the topic area: [TOPIC AREA].

Please provide a structured list of the most authoritative and current sources, including:

1. OFFICIAL GOVERNMENT SOURCES
For each official source, provide:
- Source name and description
- URL
- Issuing authority (which department/ministry)
- What it covers
- How frequently it is updated (if known)
- Any known limitations (e.g., English version may lag behind Greek)

2. OFFICIAL LEGISLATION AND REGULATIONS
- Relevant laws or regulations
- Official gazette references (where applicable)
- Any recent amendments

3. OFFICIAL GUIDANCE DOCUMENTS
- Any official guides, FAQs, or procedural documents published by the relevant authority
- URLs to downloadable forms or application guidance

4. TRUSTED SECONDARY SOURCES
- Established expat community resources, legal directories, or professional association guidance that is frequently cited and appears reliable
- Note: clearly flag these as secondary (not official) sources

5. SOURCES TO AVOID
- Any sources that appear unreliable, outdated, or potentially misleading for this topic

TOPIC AREA: [TOPIC AREA]
Specific aspects to focus on: [SPECIFIC ASPECTS]

Please verify URLs are live and note the date you last confirmed them.
```

---

## How to Use

1. Replace `[TOPIC AREA]` with the specific topic (e.g., "Cyprus immigration — Yellow Slip MEU1 process")
2. Replace `[SPECIFIC ASPECTS]` with any specific focus areas
3. Run in Perplexity
4. Save output to `assets/research-captures/source-discovery-[topic-slug]-[YYYY-MM-DD].md`
5. Add confirmed official sources to `research/sources/official-sources-cyprus.md`
6. Log in Research Log with type `Source Discovery`
