---
id: SOP-CON-001
title: Content Creation SOP
area: content
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-CON-002, SOP-CON-003]
---

# Content Creation SOP

## Purpose
Defines the end-to-end process for creating a piece of content from brief to ready-for-review draft.

## When to Use
When a content item moves to `in-production` status in the Content Pipeline.

## Prerequisites
- Content brief approved and in Notion Content Pipeline
- Related process doc(s) exist and are at least `draft` status
- Relevant KB articles available (or explicitly noted as not yet available)

---

## Steps

### 1. Read the brief
Open the content brief in Notion. Confirm:
- Content type is clear
- Target ICP(s) are identified
- Target keyword (if SEO content) is confirmed
- Related process doc is linked
- Word count target is set

### 2. Read the source material
Before writing, read:
- The related process document in full (`processes/[area]/[slug].md`)
- Any related KB articles (`knowledge/`)
- The content type definition (`content-system/content-types/[type].md`)
- The style guide sections relevant to this content type

### 3. Check the topical map
Review `content-system/topical-map/pillar-topics.md` to confirm:
- Where this piece sits in the pillar/cluster structure
- Which existing pieces it should link to (internal linking)
- Whether the angle has been covered elsewhere (anti-cannibalisation)

### 4. Draft the content
Use the appropriate page template from `content-system/templates/`:
- Guides: `guide-page-template.md`
- FAQs: `faq-page-template.md`
- Checklists: `checklist-template.md`

Write to the word count target. Do not pad. If the topic does not fill the target word count naturally, flag this in the brief rather than adding filler.

Key rules while drafting:
- Every factual claim must be traceable to a KB article or process doc
- Do not present field intelligence as official guidance
- Add the accuracy disclaimer where confidence of source material is medium or lower
- Use the correct disclaimer language from `content-system/style-guide/legal-disclaimer-rules.md`

### 5. Add internal links
Add at least 2 internal links per 1,000 words. Follow `content-system/rules/internal-linking-rules.md`.

### 6. Write meta title and description
Follow `content-system/rules/seo-rules.md` for character limits and keyword placement.

### 7. Update Notion
- Set status to `review`
- Tag the related process doc(s)
- Note any open questions or caveats in the brief

### 8. Notify reviewer
Alert the assigned reviewer that the draft is ready.

---

## Quality Check Before Moving to Review
- [ ] Word count within 10% of target
- [ ] All required sections present (per content type definition)
- [ ] No unattributed factual claims
- [ ] No official guidance presented from field sources only
- [ ] Disclaimer present where required
- [ ] Meta title and description written
- [ ] At least 2 internal links per 1,000 words
