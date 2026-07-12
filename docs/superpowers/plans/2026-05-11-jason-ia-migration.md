# Jason IA Migration Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the current 6-pillar content planning layer with Jason's ICP-pathway-first IA across the repo and Notion, driven by a single canonical URL inventory file.

**Architecture:** A new `canonical-url-inventory.md` becomes the single source of truth for all 153 pages. The topical map and content mapping files are updated to reference it. Notion Content Pipeline is populated with P0 records as the final step. All foundational files (ICP segments, process docs, agents) are untouched.

**Tech Stack:** Markdown files, git, Notion MCP tools (`mcp__claude_ai_Notion__*`), Google Drive MCP tools (`mcp__claude_ai_Google_Drive__*`)

---

## Prerequisite

Before Task 1 begins, Jason's two Google Sheets must be accessible. Ask the user to provide the URLs if not already in context. The sheets are:
- **Sheet 1** — IA workbook (ICP pathway structure, navigation, P0/P1/P2 phasing)
- **Sheet 2** — SEO sitemap (153 pages with title tags, H1s, meta descriptions, primary/secondary keywords, schema types, funnel stages, ICP assignments, internal link targets, LLM retrieval angles)

Sheet 2 is the primary source for Task 1. Sheet 1 is reference for understanding the navigation structure.

---

## File Map

| Action | File |
|--------|------|
| CREATE | `paphos-advisor/content-system/sitemap/canonical-url-inventory.md` |
| MODIFY | `paphos-advisor/content-system/topical-map/topical-map-overview.md` |
| RENAME | `paphos-advisor/content-system/topical-map/pillar-topics.md` → `pillar-topics-ARCHIVED.md` |
| CREATE | `paphos-advisor/content-system/topical-map/icp-pathway-topics.md` |
| MODIFY | `paphos-advisor/icps/mapping/icp-to-content-mapping.md` |
| NOTION | Content Pipeline — new P0 records (external, no repo file) |

---

## Task 1: Create the Canonical URL Inventory

**Files:**
- Create: `paphos-advisor/content-system/sitemap/canonical-url-inventory.md`

- [ ] **Step 1.1: Read Jason's Sheet 2**

Use `mcp__claude_ai_Google_Drive__read_file_content` or `mcp__claude_ai_Google_Drive__download_file_content` with the Sheet 2 URL. Extract all rows. Note the total page count and identify all P0-tagged rows.

- [ ] **Step 1.2: Create the inventory file**

Write `paphos-advisor/content-system/sitemap/canonical-url-inventory.md` with this exact structure:

```markdown
---
title: Canonical URL Inventory
source: Jason's SEO Sitemap (Sheet 2)
synced: 2026-05-11
total-pages: [N from sheet]
p0-count: [N from sheet]
supersedes: content-system/topical-map/pillar-topics.md
---

# Canonical URL Inventory

This file is the master reference for all pages on the Paphos Advisors website.
It supersedes `pillar-topics.md`. Do not update pillar-topics.md — update this file.

All content briefs, the content mapping, and Notion Content Pipeline records
derive from this inventory. When Jason's sheet is updated, sync here first,
then propagate changes downstream.

---

## 1. Remote Workers Pathway

| url-slug | h1 | type | phase | funnel-stage | primary-keyword | process-doc | status |
|----------|----|------|-------|-------------|----------------|------------|--------|
| /remote-workers/ | ... | hub | P0 | top | ... | none | idea |
[one row per page in this section]

---

## 2. Entrepreneurs Pathway

| url-slug | h1 | type | phase | funnel-stage | primary-keyword | process-doc | status |
|----------|----|------|-------|-------------|----------------|------------|--------|
[rows]

---

## 3. Permanent Residency Pathway

[same table structure]

---

## 4. Families Pathway

[same table structure]

---

## 5. Retirees Pathway

[same table structure]

---

## 6. Tax Residency Hub (cross-ICP)

[same table structure]

---

## 7. Property Hub (cross-ICP)

[same table structure]

---

## 8. Settling-In Hub (cross-ICP)

[same table structure]
```

Populate every row from Jason's Sheet 2. For `process-doc`: check `paphos-advisor/processes/` — if a matching PROC-XXX file exists, link it (e.g. `[PROC-IMM-001](../../../processes/immigration/yellow-slip-eu-national.md)`); otherwise write `none`. Set all `status` values to `idea` unless a brief or draft already exists.

- [ ] **Step 1.3: Audit — run these checks before committing**

Count total rows across all 8 sections. Must match the page count from Jason's sheet.

Check: all 8 section headings present.

Check: no row is missing a `url-slug` or `phase` value.

Check: no row is missing an `h1`.

Check: P0 rows count. Note this number — it is the target for Task 5 (Notion).

Fix any gaps before proceeding.

- [ ] **Step 1.4: Commit**

```
git add paphos-advisor/content-system/sitemap/canonical-url-inventory.md
git commit -m "feat(sitemap): add canonical URL inventory from Jason's SEO sitemap"
```

---

## Task 2: Update topical-map-overview.md

**Files:**
- Modify: `paphos-advisor/content-system/topical-map/topical-map-overview.md`

- [ ] **Step 2.1: Read the current file**

Read `paphos-advisor/content-system/topical-map/topical-map-overview.md` in full.

- [ ] **Step 2.2: Rewrite the file**

Replace the entire file content with the following (adapt counts from the inventory you just created):

```markdown
# Topical Map Overview

## Purpose
This document describes the content architecture for Paphos Advisors.
The canonical reference for all pages, URLs, and metadata is the
[Canonical URL Inventory](../sitemap/canonical-url-inventory.md) — consult that file first.

## Architecture

The site uses an **ICP-pathway-first** model. Each audience segment has a
dedicated pathway hub that groups all content relevant to that segment.
Cross-ICP topics that serve multiple segments have their own standalone hubs.

### ICP Pathway Hubs (5)

| Pathway | Hub URL | Primary ICP |
|---------|---------|-------------|
| Remote Workers | /remote-workers/ | ICP-02 |
| Entrepreneurs | /entrepreneurs/ | ICP-04 |
| Permanent Residency | /permanent-residency/ | ICP-05 |
| Families | /families/ | ICP-06 |
| Retirees | /retirees/ | ICP-01 |

### Cross-ICP Topic Hubs (3)

| Hub | URL | Serves |
|-----|-----|--------|
| Tax Residency | /tax-residency/ | ICP-01, ICP-02, ICP-04, ICP-05 |
| Property | /property/ | ICP-01, ICP-05, ICP-07 |
| Settling-In | /settling-in/ | All |

## Content Reference

All content planning is done through two files:

1. **[Canonical URL Inventory](../sitemap/canonical-url-inventory.md)** — master list of all [N] pages with
   URL slugs, H1s, SEO metadata, ICP assignments, phase (P0/P1/P2), and process doc links.
   This is the source of truth.

2. **[ICP Pathway Topics](icp-pathway-topics.md)** — human-readable content plan grouped by pathway,
   summarising the pages in the inventory. Use for planning conversations and prioritisation reviews.

## Archived

`pillar-topics-ARCHIVED.md` — the original 6-pillar topic plan (49 pieces).
Superseded by the canonical URL inventory. Kept for reference only — do not update it.

## Production Status

Track production status per page in the Notion Content Pipeline.
The `status` column in the inventory (idea / briefed / drafted / published)
mirrors the Notion pipeline state. Keep both in sync.
```

- [ ] **Step 2.3: Audit**

Read the file back. Confirm:
- No mentions of "6 pillars", "Pillar 1–6", or "pillar-topics.md" as the canonical reference
- All 5 pathway hubs listed
- All 3 cross-ICP hubs listed
- Pointer to inventory is present
- `pillar-topics-ARCHIVED.md` referenced (anticipating Task 3)

- [ ] **Step 2.4: Commit**

```
git add paphos-advisor/content-system/topical-map/topical-map-overview.md
git commit -m "feat(topical-map): update overview to ICP-pathway architecture"
```

---

## Task 3: Archive pillar-topics.md and create icp-pathway-topics.md

**Files:**
- Rename: `pillar-topics.md` → `pillar-topics-ARCHIVED.md`
- Create: `paphos-advisor/content-system/topical-map/icp-pathway-topics.md`

- [ ] **Step 3.1: Rename pillar-topics.md**

```
git mv "paphos-advisor/content-system/topical-map/pillar-topics.md" "paphos-advisor/content-system/topical-map/pillar-topics-ARCHIVED.md"
```

Add a note at the top of the archived file. Read the file first, then prepend:

```markdown
> **ARCHIVED 2026-05-11.** This file is the original 6-pillar content plan (49 pieces).
> It has been superseded by the Canonical URL Inventory and icp-pathway-topics.md.
> Do not update this file.

```

- [ ] **Step 3.2: Audit the archive**

Read `pillar-topics-ARCHIVED.md`. List every content piece from the old 49-piece plan.
For each piece, confirm it has a corresponding row in `canonical-url-inventory.md` (match by topic/intent, not exact title — titles may differ).

Any piece with no match in the inventory: add a note in `pillar-topics-ARCHIVED.md` at the bottom:

```markdown
## Pieces not carried forward to inventory

- [title] — [reason: out of scope / merged into X / deferred]
```

If everything maps, no note needed.

- [ ] **Step 3.3: Create icp-pathway-topics.md**

Write `paphos-advisor/content-system/topical-map/icp-pathway-topics.md`.

This is a human-readable planning overview — one section per pathway, listing pages from the inventory with their phase and primary keyword. Format:

```markdown
---
title: ICP Pathway Topics
source: canonical-url-inventory.md
updated: 2026-05-11
---

# ICP Pathway Topics

Human-readable content plan grouped by audience pathway.
For full metadata (H1, meta description, schema, internal links), see the
[Canonical URL Inventory](../sitemap/canonical-url-inventory.md).

---

## Remote Workers Pathway

**Hub:** /remote-workers/

| Page | Type | Phase | Primary Keyword |
|------|------|-------|----------------|
[one row per page in this section from the inventory]

---

## Entrepreneurs Pathway

**Hub:** /entrepreneurs/

| Page | Type | Phase | Primary Keyword |
|------|------|-------|----------------|
[rows from inventory]

---

## Permanent Residency Pathway

**Hub:** /permanent-residency/

[same structure]

---

## Families Pathway

**Hub:** /families/

[same structure]

---

## Retirees Pathway

**Hub:** /retirees/

[same structure]

---

## Tax Residency Hub (cross-ICP)

**Hub:** /tax-residency/

[same structure]

---

## Property Hub (cross-ICP)

**Hub:** /property/

[same structure]

---

## Settling-In Hub (cross-ICP)

**Hub:** /settling-in/

[same structure]
```

Populate from the inventory. The `Page` column should use the H1 from the inventory.

- [ ] **Step 3.4: Audit**

Count total rows in `icp-pathway-topics.md`. Must match total page count in the inventory.
Confirm all 8 sections present. Confirm no rows are missing a phase or primary keyword.

- [ ] **Step 3.5: Commit**

```
git add paphos-advisor/content-system/topical-map/pillar-topics-ARCHIVED.md
git add paphos-advisor/content-system/topical-map/icp-pathway-topics.md
git commit -m "feat(topical-map): replace 6-pillar plan with ICP-pathway topics; archive original"
```

---

## Task 4: Update icp-to-content-mapping.md

**Files:**
- Modify: `paphos-advisor/icps/mapping/icp-to-content-mapping.md`

The current file has tables with columns: `Content | Type | Priority | Notes`.
Two new columns are added: `url-slug` and `phase`. The `url-slug` must match a slug in the inventory exactly.

- [ ] **Step 4.1: Read the current mapping file in full**

Read `paphos-advisor/icps/mapping/icp-to-content-mapping.md` completely.

- [ ] **Step 4.2: Add columns to every table**

For each ICP section, change the table header from:

```
| Content | Type | Priority | Notes |
|---|---|---|---|
```

to:

```
| Content | Type | Priority | url-slug | phase | Notes |
|---|---|---|---|---|---|
```

For each row, add the matching `url-slug` from the inventory and its `phase` (P0/P1/P2).
To find the matching slug: look up the content title/topic in `canonical-url-inventory.md` and copy the `url-slug` value exactly.

If a content piece in the mapping has no matching slug in the inventory (i.e. it was not carried forward to Jason's IA), set `url-slug` to `pending` and `phase` to `—` and add a note in the `Notes` column: `not in inventory — review`.

- [ ] **Step 4.3: Audit**

Check: every row has a `url-slug` value (no blank cells).

Check: every `url-slug` that is not `pending` exists as a slug in the inventory. Cross-reference by searching the inventory file for each slug.

Check: every P0 page from the inventory appears in at least one ICP section of the mapping, or is flagged `new — no existing content` in the Notes column.

Fix any mismatches before committing.

- [ ] **Step 4.4: Commit**

```
git add paphos-advisor/icps/mapping/icp-to-content-mapping.md
git commit -m "feat(icps): add url-slug and phase columns to content mapping"
```

---

## Task 5: Populate Notion Content Pipeline with P0 Records

**Files:**
- No repo file changes
- Notion: Content Pipeline database

Use the P0 count confirmed in Task 1 Step 1.3 as the target. Create one record per P0 page.

- [ ] **Step 5.1: Filter inventory for P0 rows**

Read `canonical-url-inventory.md`. Extract all rows where `phase = P0`.
Build a list of: url-slug, h1, type, funnel-stage, primary-keyword, process-doc.

- [ ] **Step 5.2: Check for existing Notion records**

Use `mcp__claude_ai_Notion__notion-search` to search the Content Pipeline database for any records that already match P0 slugs or titles. Note any that already exist — do not duplicate them.

- [ ] **Step 5.3: Create Notion records for each new P0 page**

For each P0 page not already in Notion, create a Content Pipeline record using `mcp__claude_ai_Notion__notion-create-pages`.

Required fields per the content creation rules:
- **Title:** use the H1 from the inventory
- **Status:** Idea
- **Page type:** from inventory `type` column
- **Funnel stage:** from inventory `funnel-stage` column
- **Primary keyword:** from inventory `primary-keyword` column
- **URL slug:** from inventory `url-slug` column
- **ICPs:** map the pathway to the ICP segment(s) — e.g. Remote Workers pathway → ICP-02; Entrepreneurs → ICP-04; Permanent Residency → ICP-05; Families → ICP-06; Retirees → ICP-01; cross-ICP hubs → all relevant ICPs
- **Source Knowledge:** link to `process-doc` if not `none`; otherwise leave blank
- **Phase:** P0
- **Icon:** 📎 (per house rules)

Fields that can be left blank at this stage: word count, Partners, Services, Pillar/Cluster (populate when briefing begins).

- [ ] **Step 5.4: Audit**

Count Notion records created. Must equal the P0 count from Task 1 minus any pre-existing records.

Spot-check 3 records: confirm title, ICP, funnel stage, page type, and phase are all populated correctly.

- [ ] **Step 5.5: Record Notion population date in inventory header**

Open `canonical-url-inventory.md` and add a line to the frontmatter block:

```markdown
notion-p0-records-created: 2026-05-11
```

- [ ] **Step 5.6: Commit**

```
git add paphos-advisor/content-system/sitemap/canonical-url-inventory.md
git commit -m "feat(sitemap): record Notion P0 population date in inventory header"
```

---

## Final Audit (full system check)

After all 5 tasks are complete, run this cross-system check:

- [ ] Inventory page count matches Jason's sheet
- [ ] `topical-map-overview.md` references inventory and not pillar-topics
- [ ] `pillar-topics-ARCHIVED.md` has archive notice at top
- [ ] `icp-pathway-topics.md` exists and row count matches inventory
- [ ] Every row in `icp-to-content-mapping.md` has a `url-slug`
- [ ] Notion P0 record count matches inventory P0 count
- [ ] No content piece from the original 49 is orphaned without explanation
- [ ] `git log --oneline` shows 5 clean commits, one per task
