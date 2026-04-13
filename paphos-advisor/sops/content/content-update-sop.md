---
id: SOP-CON-004
title: Content Update SOP
area: content
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-CON-001, SOP-CON-002, SOP-CON-003]
---

# Content Update SOP

## Purpose
Defines how to handle updates to published content — whether triggered by a scheduled review, a regulatory change, or a reader/team flag.

## When to Use
When an existing published page needs to be updated. Distinct from creating new content.

---

## Triggers for an Update

| Trigger | Urgency |
|---|---|
| Regulation or process has changed | Immediate (within 48 hours) |
| Process doc has been revalidated with new information | Within 2 weeks |
| Scheduled review date reached | Per cadence |
| Team or client flags an inaccuracy | Within 48 hours |
| SEO performance has declined significantly | Within 1 month |

---

## Steps

### 1. Assess the scope of the update

**Minor update** — Factual correction, updated link, minor clarification. Can be made directly without a new brief.

**Major update** — Structural change, new section, outdated process steps. Treat as a new brief: create a content brief in Notion for the updated version.

### 2. Update the source material first

Before editing the live page, update the source:
- If process information has changed: update the relevant process doc in GitHub (`processes/[area]/[slug].md`)
- If a regulation has changed: update the relevant KB article in `knowledge/`
- If the change is significant: log it in CHANGELOG.md

Content should always reflect the GitHub source docs. Never update published content without updating the source first.

### 3. Make the edits

Edit the page in the CMS. Keep the existing URL (do not change URLs unless absolutely necessary — it will break inbound links and SEO).

### 4. Update the "Last updated" date

All published content should display a "Last updated" date. Update it to today.

### 5. Update Notion Content Pipeline

- Set status back to `review` if it was a major update (route through review process)
- For minor updates, keep status as `published` but log the update in the notes field
- Update the `updated` date

### 6. Update the process doc or KB article in GitHub

Increment the `updated` field in the frontmatter. If the confidence level changed, update that too.

### 7. Request re-indexing (for major updates)

Submit the updated URL to Google Search Console for re-indexing.

---

## When to Retire Instead of Update

If a piece of content is so outdated that it requires a complete rewrite, retire it:
1. Create a new content brief for the replacement
2. Once the replacement is published, redirect the old URL to the new one
3. Set the old item in Notion to `archived`
4. Do not delete old content from Notion — keep for reference
