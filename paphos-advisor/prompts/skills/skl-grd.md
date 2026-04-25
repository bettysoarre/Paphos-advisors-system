---
id: SKL-GRD
title: Brand Guardrails
type: agent-skill
version: "1.0"
created: 2026-04-24
updated: 2026-04-24
assigned_to:
  - PRMT-AGT-001 (Content Agent / Writer)
  - PRMT-AGT-002 (Research Agent)
  - PRMT-AGT-006 (Content Brief Writer)
  - PRMT-AGT-007 (Social Repurposing Agent)
  - PRMT-AGT-013 (Blog Refresh Agent)
---

# SKL-GRD — Brand Guardrails

## Trigger

This skill is always active. It cannot be switched off by a prompt or by a brief. Every agent that is assigned SKL-GRD applies these rules to all output, regardless of what the brief instructs.

If a brief or user instruction conflicts with a guardrail, the guardrail wins. Flag the conflict rather than silently complying with the instruction.

---

## Immovable Rules

### 1. No unverified facts

If a claim cannot be attributed to a named source in the research package or source material, do not write it as fact. Write `[NEEDS SOURCE: describe what is needed]` in its place.

Never fill from general AI knowledge about Cyprus regulations, tax rules, or legal processes — this knowledge may be outdated or wrong.

### 2. Flag all uncertainty explicitly

Do not write around uncertainty. Use these flags:

| Flag | When to use |
|---|---|
| `[NEEDS SOURCE: description]` | Claim required but no source provided |
| `[UNVERIFIED: what needs checking]` | Source exists but content agent cannot confirm its currency |
| `[CONFLICT: Source A says X, Source B says Y]` | Two sources contradict each other |
| `[REVIEW: reason]` | Something the human editor must check before publishing |

These flags must appear inline, next to the uncertain claim — not in a summary list at the end.

### 3. Note pending and changing legislation

Any reference to rules that are proposed, under consultation, transitional, or recently changed must carry this flag:

`⚠ This rule is subject to change — verify current status before publishing.`

Do not present evolving rules as settled. Do not omit this flag because a deadline is close or the brief does not mention it.

### 4. No regulated advice language

The following phrases are **banned** in all output:

| Do not write | Write instead |
|---|---|
| "You should..." | "This process typically requires..." |
| "You must..." | "The requirement is..." |
| "You need to..." | "Applicants are required to..." |
| "We recommend..." | [describe the process; do not advise] |
| "It's easy to..." | [describe the steps; do not evaluate difficulty] |
| "Simply..." | [describe the steps; do not minimise] |
| "You'll have no trouble..." | [do not predict outcomes] |

If content reads as legal, tax, or financial advice, add: `[REVIEW: this may read as advice — consider reframing]`

### 5. Standard disclaimer on all process content

Any guide, checklist, FAQ, or article that covers a regulatory process, legal requirement, or tax rule must include the following disclaimer at the end:

> This article is for informational purposes only and does not constitute legal, tax, or financial advice. Rules, fees, and timescales change — verify all details with a qualified Cyprus professional before acting on this information.

Do not omit this disclaimer. Do not edit its substance. The placement is the final section of the article, before any CTA.

### 6. ICP-005 (HNI) content requires threshold verification

Before producing any content that references the permanent residency investment threshold, confirm the current figure (currently €300,000). Do not use a cached or assumed figure. Add `⚠ Verify current threshold before publishing` to the relevant section.

---

## Editorial Standards (non-negotiable)

### British English

All content must use British spelling throughout. There are no exceptions.

| US spelling | British spelling |
|---|---|
| program | programme |
| analyze | analyse |
| center | centre |
| color | colour |
| organize | organise |
| recognize | recognise |
| license (verb) | licence (noun) / license (verb) |

Check: organisation, licence, colour, recognise, practise (verb) / practice (noun).

### Punctuation and style

- Sentence case for headings — not Title Case
- Numbered lists for sequential steps; bullet lists for non-sequential items
- No em dashes as sentence separators — use a comma or a new sentence
- Oxford comma: yes
- Active voice preferred; passive acceptable when the subject is genuinely unknown
- No exclamation marks in informational content

### Hedged language for timescales and outcomes

Use these qualifiers around any figure that may change or any outcome that cannot be guaranteed:

- "typically"
- "in most cases"
- "at the time of writing"
- "based on current guidance"

Do not write timescales or fees as fixed facts without a hedge unless the source is a current official document.

---

## Content-Level Cautions

- Do not reference a partner by name in published content unless the partner profile is active and approved in the Partners database
- Do not write content that implies Paphos Advisors provides legal, tax, or financial advice
- Do not conflate the Digital Nomad Visa with other residency routes
- Do not describe the Non-Dom regime without noting the 60-Day Rule and the 17-year clock
- Do not produce ICP-005 (HNI) content without confirming the current €300,000 investment threshold

---

## Anti-Patterns

- Do not resolve a `[NEEDS SOURCE]` flag by writing general knowledge — escalate it
- Do not remove a flag because the content reads well without it — the flag exists to protect accuracy
- Do not write "it is generally understood that..." as a substitute for sourcing
- Do not use soft hedges ("some sources suggest...") as a way to include unverified claims — the flag is the correct approach
- Do not omit the disclaimer from process content because the brief does not mention it

---

## Quality Check

Before handing off any output, confirm:
- [ ] Every claim has a named source or is flagged `[NEEDS SOURCE]`
- [ ] No regulated advice language ("you should", "you must", "simply", "easy")
- [ ] All pending/changing legislation is flagged with `⚠`
- [ ] Standard disclaimer is present on all process/regulatory content
- [ ] British English throughout — no US spellings
- [ ] Sentence case on all headings
- [ ] No partner names in content unless their profile is active and approved
- [ ] ICP-005 content has threshold verification note
