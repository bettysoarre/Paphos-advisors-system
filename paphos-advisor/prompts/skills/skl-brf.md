---
id: SKL-BRF
title: Brief Writing
type: agent-skill
version: "1.0"
created: 2026-04-24
updated: 2026-04-24
assigned_to:
  - PRMT-AGT-006 (Content Brief Writer)
---

# SKL-BRF — Brief Writing

## Trigger

Activate this skill when converting a research package and targeting inputs into a content brief for the Writer Agent (PRMT-AGT-001).

---

## What a Brief Is

A brief is a contract between the Brief Writer and the Writer Agent. Once approved by a human, the Writer follows the brief exactly. The brief must make every editorial decision so that the Writer focuses on writing — not planning.

A brief that leaves any section vague, blank, or marked "TBD" is an incomplete brief. An incomplete brief produces an incomplete article.

---

## Execution Steps

1. Confirm all required inputs are present before starting (see Inputs section below). If any are missing, request them.
2. Read the research package in full before writing any section.
3. Identify the single best angle for this piece — one sentence: "This article helps [specific person] understand/do [specific thing] so that they [specific outcome]." If you need more than one clause, the angle is too broad.
4. Select the ICP segment and journey stage from the ICP files (`icps/segments/`). Do not invent ICP characteristics.
5. Write all sections of the brief template in sequence. Do not skip sections.
6. Run the quality check before marking the brief as complete.

---

## Required Inputs

Request these before starting. If any are missing, block and ask.

| Input | Required |
|---|---|
| Approved research package | Yes |
| Target keyword | Yes — if unknown, propose one and state reasoning |
| Target ICP (ICP-001 through ICP-006) | Yes |
| Content type | Yes |
| Word count target | Yes — if unknown, apply content-type default |
| Related process IDs (e.g. PROC-IMM-001) | If applicable |
| Available internal links | If applicable |
| CTA instruction | If provided — if not, select from standard CTA types |

---

## One Angle Per Brief

Every brief covers one angle. If the research supports multiple angles, write separate briefs.

The angle test: complete this sentence in one clause —
*"This article helps [specific person] understand/do [specific thing] so that they [specific outcome]."*

If you need two clauses, split the brief.

---

## ICP Selection

Every brief is written for one ICP at one stage of their journey. "Anyone relocating to Cyprus" is not an ICP.

Specify:
- Which ICP segment (ICP-001 through ICP-006)
- Where they are in their journey: just researching / ready to act / mid-process / post-arrival
- What they already know (do not brief the Writer to explain concepts the reader already knows)
- What they are anxious about (shapes tone and what reassurances to include)

| ICP | Lead angle | Tone note |
|---|---|---|
| ICP-001 (UK National Retiree) | What is still possible post-Brexit; address anxiety first | Reassuring, step-by-step, plain language |
| ICP-002 (EU National Remote Worker) | Tax saving or process simplicity number first | Direct, practical, numbers-forward |
| ICP-003 (Non-EU Digital Nomad) | Eligibility criteria stated clearly | Honest about restrictions; no over-promising |
| ICP-004 (Entrepreneur) | Structure and effective rate | Professional, detail-tolerant, full picture |
| ICP-005 (HNI Permanent Residency) | Security, timeline, and what the investment buys | Formal, concise, premium register |
| ICP-006 (Family Relocating) | Children's setup first, then adult process | Warm, comprehensive, acknowledge emotional weight |

---

## SEO Requirements in the Brief

The SEO section is not optional and is not the Writer's responsibility to figure out. Every brief must provide:

- The exact primary keyword (the phrase a reader would type into Google)
- A proposed title tag under 60 characters that includes the primary keyword
- A proposed meta description under 155 characters that includes the keyword and ends with a value statement
- Secondary keywords to include naturally in the body
- The required schema type: HowTo / FAQPage / Article / none
- Internal links: specific pages to link to, with suggested anchor text

If keyword data is not provided, select the most likely search phrase for this ICP at this journey stage. State your reasoning so the human reviewer can override it.

---

## Structure Is the Writer's Map

The outline in the Structure section defines what the article contains. The Writer follows the H2s and H3s exactly. This means:

- Every H2 must be specific — no placeholders like "Background" or "Overview"
- Include approximate word count per major section
- For process content: H2 structure must follow the actual process sequence
- For FAQ content: questions must be what the ICP actually asks — pull from ICP segment files
- For comparison content: must include a Quick Comparison table section and a Decision Guide section

---

## Source Completeness

The brief must list every source the Writer needs. The Writer does not search for sources — they write from what the brief provides.

If a key point has no source:
- Mark the point: `[NEEDS SOURCE: describe what is needed]`
- Note in Source Material: `[RESEARCH GAP: this section requires additional research before writing can begin]`
- Block the brief from passing to the Writer until the gap is resolved

---

## BRIEF BLOCKED Escalation

If the research package has gaps that prevent a complete brief:
- Output `[BRIEF BLOCKED]` with a list of each gap
- Do not produce a partial brief — a partial brief produces a partial article
- The human routes the gap back to the Research Agent

---

## Brief Template

```
---
id: brief-[type]-[slug]
title: "[Working title]"
content_type: [type from taxonomy]
target_keyword: "[exact keyword phrase]"
search_intent: [informational | navigational | commercial | transactional]
target_icp:
  - [ICP-00X]
related_processes:
  - [PROC-XXX-NNN or "none"]
source_knowledge:
  - [KB-XXX-NNN or "none"]
status: briefed
created: [YYYY-MM-DD]
updated: [YYYY-MM-DD]
---

## Objective
[2–3 sentences: what this piece achieves, who it is for, what business goal it serves]

---

## Target Audience
[ICP segment, journey stage, what they know, what they are anxious about, what objections they have]

---

## Key Points to Cover

**Must include:**
- [Point 1 — specific, not vague]
- [Point 2]

**Out of scope / avoid:**
- [e.g. "Do not cover Category 6.2 residency — separate article"]

---

## Source Material
- [Internal: PROC-XXX-NNN — [title] — [specific sections to reference]]
- [Internal: KB-XXX-NNN — [title]]
- [External: [source name] — [URL] — [what it is used for]]
- [RESEARCH GAP: [description, if applicable]]

---

## Structure / Outline

### [H2: exact heading text]
[What to cover — approximate word count]

  #### [H3: if applicable]
  [What to cover]

---

## SEO Requirements
**Primary keyword:** [exact phrase]
**Secondary keywords:** [comma-separated]
**Title tag:** [under 60 chars]
**Meta description:** [under 155 chars — ends with value statement]
**Schema:** [HowTo | FAQPage | Article | none]
**Internal links:**
- [Page title] → anchor text: "[suggested text]"

---

## Call to Action
**Primary CTA:** [exact CTA copy]
**Destination:** [page or action]
**Placement:** [end of article / mid-article after section X]

---

## Notes
[Tone guidance, content sensitivities, editorial decisions the human reviewer might want to override]
```

---

## Anti-Patterns

- Do not write a vague objective like "explain what non-dom is" — specify who needs to understand it and why
- Do not leave the SEO section blank or the title tag empty
- Do not pass a brief to the Writer if any Key Point is marked `[NEEDS SOURCE]`
- Do not cover two distinct angles in one brief — split into two
- Do not write "Writer to decide on structure" — structure is the brief's job
- Do not use internal jargon in the title tag or meta description
- Do not brief process content without specifying the related PROC-* document

---

## Quality Check

Before passing the brief to the Writer, confirm:
- [ ] All sections filled — no "TBD" or blank sections
- [ ] Primary keyword is a real search phrase, not an internal term
- [ ] Title tag is under 60 characters and includes the primary keyword
- [ ] Meta description is under 155 characters and ends with a value statement
- [ ] Every "Must include" point has a source in the Source Material section
- [ ] No `[RESEARCH GAP]` remains unresolved
- [ ] ICP and journey stage are specific, not generic
- [ ] Structure matches the content-type requirements
- [ ] No `[BRIEF BLOCKED]` items outstanding
