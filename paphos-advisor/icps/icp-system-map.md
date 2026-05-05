---
id: ICP-MAP-000
title: "Paphos Advisors ICP System Map v1"
type: system-overview
created: 2026-05-05
updated: 2026-05-05
owner: "lead-advisor"
related_files:
  - icps/_index.md
  - icps/framework/segmentation-model.md
  - icps/framework/scoring-criteria.md
  - icps/mapping/icp-to-content-mapping.md
  - icps/mapping/icp-to-service-mapping.md
  - icps/mapping/icp-pain-point-content-matrix.md
  - system/taxonomies/icp-segments.yaml
---

# Paphos Advisors ICP System Map v1

Single reference document for the full 9-segment ICP system. Use this to understand segment relationships, commercial priorities, and how the system hangs together before working with individual segment files or mapping documents.

---

## The 9 Segments at a Glance

| ID | Name | Priority | Status | Revenue Role |
|---|---|---|---|---|
| ICP-SEG-001 | UK National Retiree | P2 | active | High volume, property commission on 12–24 month lag |
| ICP-SEG-002 | EU National — Remote Worker | P1 | active | Highest revenue — multi-service tax + immigration bundle |
| ICP-SEG-003 | Non-EU Digital Nomad | P3 | active | Lower revenue — single process, fewer referrals |
| ICP-SEG-004 | Entrepreneur — Company Formation | P3 | active | High value — strongest tax advisor referral in system |
| ICP-SEG-005 | HNI — Permanent Residency | Unranked | active | Highest per-case value — €300k+ property commission |
| ICP-SEG-006 | Family Relocating with Children | Unranked | active | Volume across multiple service categories |
| ICP-SEG-007 | Property Speculators | Unranked | draft | Property commission as primary event |
| ICP-SEG-008 | Related Partners | Unranked | draft | B2B only — indirect revenue multiplier |
| ICP-SEG-009 | Low Budget Escapers | Unranked | draft | Content traffic + long-term nurture |

---

## Commercial Cluster View

### Primary commercial cluster (1/2/4/5/6)
These five segments form the design and content priority set. Together they account for essentially all direct advisory revenue and most partner referral commission.

**ICP-002 — EU Remote Worker** is P1: the highest-revenue segment due to the multi-service bundle (Yellow Slip + 60-day rule + non-dom). Tax advisor referral is the most valuable single referral in the system.

**ICP-004 — Entrepreneur** ranks alongside ICP-002 for per-case value because corporate + personal tax advisory is the richest referral package. Company formation content is the strongest differentiator in the market.

**ICP-005 — HNI** has the highest individual case value — the €300k+ property commission is the single largest revenue event — but volume is lower and the segment requires a distinct tone and partner network (specialist immigration lawyers, developer contacts).

**ICP-006 — Family** generates volume across immigration, school, property, and removal referrals. The mixed-nationality couple is a high-conversion lead type because no single competitor handles both the EU and UK parent processes simultaneously.

**ICP-001 — UK Retiree** is P2: large volume, strong community presence, and a reliable property purchase 12–24 months post-arrival. The immigration process (Category F) is more complex than Yellow Slip, which increases advisory value.

### Secondary and special-case segments (3/7/9)
**ICP-003 — Non-EU Digital Nomad** is P3: one main process, fewer referrals, lower revenue, but the comparison-content strategy has high SEO value and positions Paphos Advisors against competitors in nomad forums.

**ICP-007 — Property Speculators** is opportunistic: high search intent, property commission as the primary event, immigration and tax advisory as downstream. These leads are savvy and research-led — authority content (title deed risk, developer due diligence, yield data) is the acquisition mechanism.

**ICP-009 — Low Budget Escapers** is a nurture-only segment: no immediate advisory revenue, but high content traffic that supports SEO for ICP-001/002, and long-term referral value from word-of-mouth.

### Stakeholder segment (8)
**ICP-008 — Related Partners** is not a marketing ICP. It defines how Paphos Advisors engages the B2B layer of its referral network — lawyers, agents, accountants, community connectors. The primary content output for this segment is a "Work with us / Partner" page, not articles. Revenue impact is indirect but significant.

---

## Segment Relationship Map

```
ICP-001 (UK Retiree)
  ↔ ICP-005 (HNI) — both property buyers; HNI has higher investment threshold
  ↔ ICP-006 (Family) — UK parent in mixed-nationality family triggers Category F

ICP-002 (EU Remote Worker)
  ↔ ICP-004 (Entrepreneur) — remote workers who also want a Cyprus company straddle both
  ↔ ICP-006 (Family) — EU parent in mixed-nationality family follows Yellow Slip route

ICP-003 (Non-EU Digital Nomad)
  ↔ ICP-004 (Entrepreneur) — significant passive income shifts to ICP-004; active company to ICP-004
  ↔ ICP-005 (HNI) — high net worth non-EU nationals may qualify for Category 6.2 instead of DNV
  ↔ ICP-009 (Low Budget Escapers) — income below DNV threshold re-routes here

ICP-004 (Entrepreneur)
  ↔ ICP-002 (EU Remote Worker) — EU directors often combine personal residency + company
  ↔ ICP-005 (HNI) — high-value clients with both company and personal PR needs

ICP-005 (HNI)
  ↔ ICP-007 (Property Speculators) — ICP-005 requires €300k new developer only; ICP-007 is broader

ICP-007 (Property Speculators)
  ↔ ICP-001/002 — subset will need immigration/tax once they decide to spend significant time in Cyprus
  ↔ ICP-005 — buyers at €300k+ on new developer stock may qualify for PR route

ICP-008 (Related Partners)
  ↔ All segments — feeds qualified referrals into ICP-001 through 007
```

---

## Process Cluster by Segment

| Process Cluster | Segments |
|---|---|
| Category F (non-EU self-sufficient) | ICP-001 (Critical), ICP-004 non-EU directors (High) |
| Yellow Slip / MEU1 (EU nationals) | ICP-002 (Critical), ICP-006 EU parent (Critical), ICP-004 EU directors (High) |
| Digital Nomad Visa | ICP-003 (Critical) |
| Category 6.2 Permanent Residency | ICP-005 (Critical) |
| 60-Day Rule + Non-Dom | ICP-002, ICP-004, ICP-005 (Critical); ICP-001, ICP-003 (Medium) |
| Company Formation | ICP-004 (Critical) |
| Property Purchase | ICP-005 (Critical), ICP-001, ICP-007 (High) |
| School Registration | ICP-006 (Critical) |
| GESY Registration | ICP-001, ICP-002, ICP-006 (High); others (Medium–Low) |

---

## Revenue Logic Summary

The Paphos Advisors revenue model is referral-led. There are no direct service fees listed as primary income — all revenue flows through partner referrals triggered by the advisory relationship.

**Highest-value referral events (in order):**
1. Property purchase commission (€300k+ for ICP-005; market rate for ICP-001/007)
2. Tax advisor referral — ICP-004 (corporate + personal), ICP-002 (non-dom + 60-day), ICP-005 (wealth structuring)
3. Immigration lawyer referral — ICP-005 (Category 6.2), ICP-001 (Category F), ICP-003 (DNV)
4. Long-term rental referral — ICP-002, ICP-006 (MEU1-compliant lease; first practical blocker for many leads)
5. Private health insurance referral — ICP-001, ICP-003, ICP-005 (required for applications)

**Time-to-revenue profile:**
- ICP-002, ICP-003, ICP-004: Fast (weeks to months) — immigration and tax referrals trigger quickly
- ICP-001, ICP-006: Medium (months) — immigration first, property 12–24 months later
- ICP-005: Slow but highest value (3–12 months from first contact to property purchase)
- ICP-007: Variable (can be fast if buyer is ready; may be 6–18 months if speculative)

---

## Content Strategy Shorthand

Each segment maps to a dominant content type and a primary discovery mechanism:

| Segment | Primary Content Type | How They Find Us |
|---|---|---|
| ICP-001 | Guides + FAQs (Brexit, pension tax, Category F) | Search — "moving to Cyprus after Brexit" |
| ICP-002 | How-to process guides (Yellow Slip, non-dom, 60-day) | Search — "Yellow Slip Cyprus" |
| ICP-003 | Comparisons + explainers (DNV eligibility, Cyprus vs Portugal) | Search + nomad forums |
| ICP-004 | Technical explainers (company formation, IP Box, non-dom for directors) | Search + professional referral |
| ICP-005 | Authoritative guides (Category 6.2, developer due diligence) | Referral + nationality-specific search |
| ICP-006 | Practical guides (schools, vaccination, family areas) | Search — "schools in Paphos" |
| ICP-007 | Market intelligence (yields, title deeds, red-loan properties) | Search — "property investment Cyprus" |
| ICP-008 | Partner page + regulatory updates | Direct + professional network |
| ICP-009 | Cost of living + Category F requirements | Search — "cheapest places to live in Cyprus" |

**Six topical pillars:** Moving to Cyprus (master entry point) | Immigration & Residency | Tax & Financial Planning | Buying Property in Cyprus | Setting Up a Business | Living in Paphos

**Three content-type pillars:** Method (how-to guides, process explainers) | Housekeeping (checklists, document lists) | Lifestyle (area guides, cost of living, schools)

---

## Content Red Lines

These apply across all ICP segments and all content formats. They are standing constraints, not per-segment decisions.

**Never:**
- Frame any tax structure as avoidance, arbitrage, or a workaround — Cyprus is a legitimate EU jurisdiction with real legal structures; all advisory must be positioned in compliance terms
- Signal a political stance on any topic, including Brexit, EU membership, Middle East politics, or Cypriot domestic affairs
- Use language that implies Cyprus has been "taken over" by expats or foreign buyers — any framing that sets expats against locals is disqualifying
- Denigrate or diminish Cypriot people, institutions, or culture in any content format, including social media

**Irish HNW audience note:**
Irish HNW individuals are EU nationals (Yellow Slip residency route) but motivationally closer to ICP-005. Content for this audience may reference EU/political instability as a driver in social media, but the website must remain neutral — focused on stability, structure, and opportunity rather than explicit political commentary.

**Positioning rule for all ICP content:**
Paphos Advisors must be explicitly and visibly Cypriot-friendly. Content should reflect that we are operating within the local ecosystem, not on behalf of inbound foreign capital against local interests.

---

## Known Gaps and Validation Status

| Item | Status |
|---|---|
| ICP-001 through 006 segment files | Active — 14-section schema (updated 2026-05-05) |
| ICP-007 through 009 segment files | Draft — from Phase 0 research (2026-05-05); needs real client data validation |
| Market sizing (volume, revenue potential per ICP) | Not yet done — qualitative priorities only |
| Journey maps (awareness → immigration → arrival → property) | Not yet done |
| Evidence tags (verbatim questions linked to source) | Not yet done |
| "Buying property in Cyprus" process doc | Does not yet exist — flagged for creation |
| ICP-007/008/009 pain-point mapping | Draft stubs in icp-pain-point-content-matrix.md |
| icp-segments.yaml | Updated 2026-05-05 — all 9 segments present |

---

## Key File Locations

| File | Purpose |
|---|---|
| [icps/_index.md](_index.md) | Segment registry — all 9 files and their status |
| [icps/framework/segmentation-model.md](framework/segmentation-model.md) | How segments are defined — 4 dimensions, priority rationale |
| [icps/framework/scoring-criteria.md](framework/scoring-criteria.md) | Intake scoring — 4-dimension fit, segment assignment table |
| [icps/mapping/icp-to-content-mapping.md](mapping/icp-to-content-mapping.md) | Content priorities per segment |
| [icps/mapping/icp-to-service-mapping.md](mapping/icp-to-service-mapping.md) | Service routing and partner referral priorities |
| [icps/mapping/icp-pain-point-content-matrix.md](mapping/icp-pain-point-content-matrix.md) | Pain point → content across 3 pillars |
| [system/taxonomies/icp-segments.yaml](../system/taxonomies/icp-segments.yaml) | Machine-readable segment taxonomy |
| [content-system/strategy/audience-needs-mapping.md](../content-system/strategy/audience-needs-mapping.md) | ICP needs mapped to content pillars and funnel stages |
| [research/frameworks/](../research/frameworks/) | Research and validation framework — governs how all ICP process and regulatory claims are sourced and tiered (process-research-framework.md, regulatory-monitoring-framework.md, field-intelligence-framework.md) |
| [research/validation/](../research/validation/) | Source and process validation checklists — knowledge-accuracy-criteria.md, source-validation-checklist.md, process-validation-checklist.md |
| [research/sources/](../research/sources/) | Registered source registry and tiered source lists — source-registry.csv, official-sources-cyprus.md, third-party-sources.md |
