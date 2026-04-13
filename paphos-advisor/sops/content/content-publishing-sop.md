---
id: SOP-CON-003
title: Content Publishing SOP
area: content
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-CON-001, SOP-CON-002, SOP-CON-004]
---

# Content Publishing SOP

## Purpose
Defines the steps to publish approved content to the website and update all related records.

## When to Use
When a content item reaches `approved` status in the Content Pipeline.

---

## Steps

### 1. Final pre-publish check
Before uploading:
- [ ] Status in Notion is `approved`
- [ ] Meta title and description are finalised
- [ ] All internal links have been verified (target pages exist and are live)
- [ ] Disclaimer language is correct and present
- [ ] Any images or assets are optimised and have alt text

### 2. Publish to website
Follow the website's CMS workflow (to be documented separately once the website platform is confirmed).

Key requirements:
- Set the canonical URL
- Add the meta title and description
- Apply the correct page template
- Set the publish date
- Tag with relevant categories/topics in the CMS

### 3. Verify live page
After publishing:
- [ ] Page loads correctly at the expected URL
- [ ] Meta title and description appear correctly in browser tab and search preview
- [ ] All internal links resolve correctly
- [ ] No formatting issues visible on desktop and mobile
- [ ] Disclaimer is visible and correctly worded

### 4. Update Notion Content Pipeline
- Set status to `published`
- Record the published URL in the `Published URL` field
- Record the publish date

### 5. Update related records
- If the content is based on a specific process doc, update the process doc's `published_date` field in GitHub
- If the content introduces a new FAQ, add the FAQ to the relevant KB article or FAQ file in `knowledge/faqs/`

### 6. Submit to Google Search Console
For new pages or significantly updated pages:
- Request indexing via Google Search Console
- Note the submission date in Notion

### 7. Internal linking update
After publishing, check existing content for opportunities to add internal links to the new page. Follow `content-system/rules/internal-linking-rules.md`.

---

## Post-Publish
Set a review reminder per `content-system/rules/update-cadence-rules.md`:
- Evergreen content: 12 months
- Time-sensitive / regulatory content: 3-6 months
- News updates: No scheduled review (replaced rather than updated)
