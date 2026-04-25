---
id: SKL-SEO
title: Formatting & SEO
type: agent-skill
version: "1.0"
created: 2026-04-24
updated: 2026-04-24
assigned_to:
  - PRMT-AGT-001 (Content Agent / Writer)
  - PRMT-AGT-006 (Content Brief Writer)
---

# SKL-SEO — Formatting & SEO

## Trigger

Activate this skill whenever the agent is producing or briefing a piece of website content. Applies to all content types: guides, FAQs, checklists, comparisons, blog posts, service pages, landing pages, and lifestyle content.

---

## Required Elements (Every Draft)

Every piece of content must include all of the following. Missing any element is an error.

| Element | Specification |
|---|---|
| Frontmatter | Title, slug, content type, ICP, pillar/cluster, process docs, status: draft |
| Meta title | 50–60 characters; includes primary keyword; does not repeat H1 word-for-word |
| Meta description | 150–160 characters; includes primary keyword; ends with a clear value proposition |
| H1 | One per page; sentence case; matches search intent of the primary keyword |
| Schema scaffold | Included at the bottom of the draft — type depends on content (see below) |

---

## Heading Hierarchy

- **H1** — page title only; one per page
- **H2** — major section headings; must be specific and reflect real content (not "Background" or "Overview")
- **H3** — sub-sections within an H2; use when a section has distinct sub-topics
- **H4 and below** — use sparingly; only when structure genuinely requires it

All headings: sentence case. No title case.

---

## Meta Title Rules

1. Include the exact primary keyword
2. Keep to 50–60 characters (count spaces)
3. Do not use internal jargon — write for how a reader would search
4. Do not duplicate the H1 word-for-word — vary the phrasing slightly
5. Do not end with the site name unless the brief specifies it

**Example:** `Cyprus 60-day tax residency rule explained` (43 chars) ✓
**Not:** `Cyprus Tax Residency — The 60-Day Rule Guide for Expats Moving to Cyprus in 2025` (too long) ✗

---

## Meta Description Rules

1. Include the primary keyword naturally (do not stuff)
2. Keep to 150–160 characters (count spaces)
3. End with a clear value statement — what will the reader know or be able to do?
4. Write in plain language — no jargon, no brand-speak
5. Do not use the same phrasing as the meta title

**Example:** `Understand Cyprus's 60-day tax residency rule: who qualifies, what it requires, and how to apply it alongside non-dom status.` ✓

---

## Schema Type Selection

| Content type | Schema to use |
|---|---|
| Guide / process explainer | `HowTo` |
| FAQ page | `FAQPage` |
| Comparison | `Article` |
| Blog post | `Article` |
| Service page | `Service` or none |
| Landing page | none |
| Checklist | `HowTo` |
| Lifestyle | `Article` |

Include a scaffold at the bottom of the draft. The schema is a placeholder for the developer — the agent writes the structure, not valid JSON-LD, unless instructed otherwise.

**HowTo scaffold:**
```
<!-- HowTo schema scaffold
@type: HowTo
name: [H1 text]
description: [meta description text]
step[1]: [first H2 step heading] — [one-line description]
step[2]: ...
-->
```

**FAQPage scaffold:**
```
<!-- FAQPage schema scaffold
@type: FAQPage
question[1]: [question text] | answer[1]: [answer text — 50 words max]
question[2]: ...
-->
```

---

## Internal Links

The brief specifies which pages to link to. When writing:
- Insert a link placeholder at the first natural mention of the linked topic
- Format: `[INTERNAL LINK: Page Title → anchor text: "suggested anchor text"]`
- Do not use "click here" or "read more" as anchor text — use descriptive text
- Do not link to the same page more than once in the same article unless the brief instructs it

---

## Word Count by Content Type

Word count targets are defined in SKL-BRF (`paphos-advisor/prompts/skills/skl-brf.md`), which is the single source of truth. When checking whether a draft meets its word count target, refer to the target specified in the brief — not a generic default.

If no brief word count is present, the content-type defaults are in SKL-BRF under "Required Inputs".

---

## Secondary Keywords

Use secondary keywords naturally in the body — do not repeat them mechanically. The brief specifies which secondary keywords to include. Do not invent keywords not listed in the brief.

Placement guidance:
- H2s and H3s: use secondary keywords where they fit naturally — do not force them
- Body paragraphs: at least one natural occurrence per secondary keyword
- Do not cluster keywords in one section — distribute across the article

---

## Anti-Patterns

- Do not leave meta title or meta description blank — the Writer cannot produce correct output without them
- Do not use Title Case in headings
- Do not use "click here" as anchor text
- Do not repeat the same internal link more than once per article
- Do not write a meta description that is just a restatement of the title
- Do not select a schema type not listed above without flagging it
- Do not pad word count to hit the target — accuracy over length

---

## Quality Check

Before handing off content, confirm:
- [ ] Meta title is 50–60 characters and includes the primary keyword
- [ ] Meta description is 150–160 characters and ends with a value statement
- [ ] H1 is sentence case and matches search intent
- [ ] All headings are sentence case — no Title Case
- [ ] Schema scaffold is included and matches content type
- [ ] Internal link placeholders are present for every link specified in the brief
- [ ] Secondary keywords appear naturally — not clustered
- [ ] Word count falls within the content-type range
