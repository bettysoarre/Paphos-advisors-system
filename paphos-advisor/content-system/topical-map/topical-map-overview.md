# Topical Map Overview

## Purpose
This document describes the content architecture for Paphos Advisors.
The canonical reference for all pages, URLs, and metadata is the
[Canonical URL Inventory](../sitemap/canonical-url-inventory.md) — consult that file first.

---

## Architecture

The site uses an **ICP-pathway-first** model. Each audience segment has a dedicated pathway hub
grouping all content relevant to that segment. Cross-ICP topics that serve multiple segments
have their own standalone hubs. A third layer — Services, Experts, Locations, and Support pages
— provides functional pages that cross-link across pathways.

---

## ICP Pathway Hubs (8)

| Pathway | Hub URL | Primary ICP | Phase |
|---------|---------|-------------|-------|
| Remote Workers | /remote-workers | ICP-002 | P0 |
| Entrepreneurs | /entrepreneurs | ICP-004 | P0 |
| Permanent Residency | /permanent-residency | ICP-005 | P0 |
| Families | /families | ICP-006 | P0 |
| Retirees | /retirees | ICP-001 | P0 |
| Digital Nomads | /digital-nomads | ICP-003 | P2 |
| Property Investors | /property-investors | ICP-007 | P2 |
| Budget Movers | /budget-movers | ICP-009 | P2 |

---

## Cross-ICP Topic Hubs (4)

| Hub | URL | Serves | Phase |
|-----|-----|--------|-------|
| Tax & Residency | /tax-residency | ICP-001, ICP-002, ICP-004, ICP-005 | P0 |
| Property | /property | ICP-001, ICP-005, ICP-006, ICP-007 | P0 |
| Settling In | /settling-in | All | P1 |
| Resources | /resources | All | P0 |

---

## Supporting Sections

| Section | URL | Phase | Notes |
|---------|-----|-------|-------|
| Services | /services | P0 | BOFU conversion pages; one per service category and sub-service |
| Experts | /experts | P0 hub, P1 sub-pages | Partner category pages for trust and referral conversion |
| Locations | /locations | P0 hub, P1/P2 sub-pages | Area guides; support property and lifestyle decisions |
| Compare | /compare | P1/P2 | Comparison articles; decision-stage content |
| Glossary | /glossary | P1 | Plain-English definitions; TOFU / LLM retrieval |
| FAQ | /faq | P0 hub, P1 sub-pages | Structured answers; high TOFU search demand |
| Tools | /tools | P1 | Lead magnets and interactive tools |
| Blog | /resources/blog | P1/P2 | Weekly/seasonal news and lifestyle posts; TOFU, distinct cadence from evergreen pages |
| Core | /, /about, /contact, /start, /legal | P0 | Utility and trust pages |

---

## Content Reference Files

| File | Purpose |
|------|---------|
| [Canonical URL Inventory](../sitemap/canonical-url-inventory.md) | Master list of all 153 pages — URL slugs, H1s, types, phases, funnel stages, primary keywords, ICP assignments, process doc links, status. **This is the source of truth.** |
| [ICP Pathway Topics](icp-pathway-topics.md) | Human-readable content plan grouped by pathway and section — use for planning and prioritisation reviews |
| [ICP-to-Content Mapping](../../icps/mapping/icp-to-content-mapping.md) | Maps each ICP segment to specific content pieces with priority and URL slug |

---

## Archived

`pillar-topics-ARCHIVED.md` — the original 6-pillar topic plan (49 pieces, 6 pillars).
Superseded by the canonical URL inventory. Kept for reference only — do not update it.

---

## Production Status

Track production status per page in the Notion Content Pipeline.
The `status` column in the inventory (`idea / briefed / drafted / published`)
mirrors the Notion pipeline state — keep both in sync when a brief is created or a draft moves forward.
