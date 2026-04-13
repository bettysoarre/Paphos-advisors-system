---
id: SOP-KNW-002
title: Knowledge Review SOP
area: knowledge
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-KNW-001, SOP-KNW-003, SOP-RES-004]
---

# Knowledge Review SOP

## Purpose
Defines how to review knowledge articles for continued accuracy and relevance.

## Cadence
From `system/governance/review-cadences.md`:
- High confidence articles: 12-month review cycle
- Medium confidence articles: 6-month review cycle
- Low confidence articles: 3-month review cycle or until resolved

---

## Steps

### 1. Identify articles due for review
In Notion Knowledge Base, filter by `Next Review Due` ≤ today. Work through the list in priority order (low confidence first, then by topic area relevance to active cases).

### 2. Check whether the claim is still valid
For official knowledge articles:
- Navigate to the source URL
- Confirm the page content matches the claim in the article
- Check the page's "last updated" date

For field knowledge articles:
- Is there any newer intelligence from partner interviews that contradicts or updates this claim?
- Has a recent research session produced conflicting information?

### 3. Assess the outcome

**Claim is still valid:**
- Update `updated` and `last_reviewed` dates in frontmatter
- Set `next_review_due` based on the cadence
- Add a `validation_history` entry if using the template with that section

**Claim needs updating:**
- Update the body of the article
- Update confidence level if it has changed
- Note what changed and why in the frontmatter or a comment
- Set status to `Validated` after update

**Claim is no longer valid:**
- If superseded by better information: update the article
- If the process it relates to no longer exists: set status to `Archived`

### 4. Update Notion
- Update `Last Reviewed` and `Next Review Due` in the Notion Knowledge Base record
- Update `Status` if changed

### 5. Check for downstream impact
If the claim changed:
- Is it referenced in any published content? If so, create a content update task.
- Is it referenced in a process doc? If so, update the process doc.
