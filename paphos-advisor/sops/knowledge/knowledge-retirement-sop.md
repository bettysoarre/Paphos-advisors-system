---
id: SOP-KNW-003
title: Knowledge Retirement SOP
area: knowledge
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-KNW-001, SOP-KNW-002]
---

# Knowledge Retirement SOP

## Purpose
Defines how to retire a knowledge article that is no longer current or relevant.

## When to Retire (Not Update)
Retire an article when:
- The process it relates to no longer exists (e.g., a visa type has been abolished)
- The information is so fundamentally different from current reality that the article would be misleading even with updates
- It has been fully superseded by a newer, higher-confidence article on the same topic

Do not retire articles simply because they are old. If the claim is still valid, update the review date instead.

---

## Steps

### 1. Confirm retirement is the right action
Before retiring, ask:
- Is there any scenario in which this information is still useful (e.g., historical context, transitional arrangements)?
- Has it been superseded by a specific replacement article?

### 2. Note the retirement reason
Add a comment at the top of the file (below frontmatter):
```
<!-- RETIRED [YYYY-MM-DD]: [Reason. Reference to replacement article if applicable.] -->
```

### 3. Update frontmatter
- Set `status` to `archived`
- Update `updated` date

### 4. Move to archive folder
Move the file to `assets/_archive/knowledge/[original-path]`. Do not delete.

### 5. Update Notion
- Set status to `Archived` in the Knowledge Base record
- Note the retirement reason in the Notes field

### 6. Check for downstream references
- Search for the KB article ID in process docs: `grep -r "KB-XXX-NNN" processes/`
- Check if it is referenced in any published content
- Update any references to point to the replacement article or remove them

### 7. Log in CHANGELOG if the retirement is significant
If the retirement reflects a regulatory change (e.g., a process has been abolished), log it in CHANGELOG.md.
