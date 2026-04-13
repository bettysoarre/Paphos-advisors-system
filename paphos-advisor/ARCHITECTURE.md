# System Architecture — Paphos Advisors

## Purpose

This document explains the structural design of the Paphos Advisors knowledge and operations system. It is the meta-reference for understanding how all the pieces fit together.

---

## Core Design Principles

**1. Separation of definition from operation**
The repository defines *what things are* and *how things should work*. Notion is where work actually happens. This separation means definitions can be versioned, reviewed, and kept clean — without being disrupted by day-to-day operational noise.

**2. Single source of truth**
Every canonical definition (process, taxonomy, schema, rule) exists in one place. If it is not in this repo, it is not canonical. Notion databases are derived from the schemas defined here.

**3. Structured knowledge accumulation**
Raw intelligence (from interviews, research sessions, official sources) flows through a defined pipeline — extraction → structuring → validation → publication. Nothing goes to clients without passing through this pipeline.

**4. Confidence-aware outputs**
Every piece of knowledge carries a confidence level (high / medium / low / unverified). This is enforced at the data layer, not left to individual judgement.

---

## System Layers

```
┌─────────────────────────────────────────────────────┐
│                    CLIENT LAYER                      │
│         Website content, guides, checklists         │
└────────────────────────┬────────────────────────────┘
                         │ derived from
┌────────────────────────▼────────────────────────────┐
│                  OPERATIONAL LAYER                   │
│    Notion — cases, content pipeline, partners,      │
│             research log, knowledge base            │
└────────────────────────┬────────────────────────────┘
                         │ governed by
┌────────────────────────▼────────────────────────────┐
│                  DEFINITION LAYER                    │
│    This repository — processes, SOPs, schemas,      │
│    taxonomies, templates, rules, ICP profiles       │
└────────────────────────┬────────────────────────────┘
                         │ populated by
┌────────────────────────▼────────────────────────────┐
│                   INTELLIGENCE LAYER                 │
│  Research sessions (Perplexity), partner interviews  │
│  (Plaud Note), official sources, field observations  │
└─────────────────────────────────────────────────────┘
```

---

## Repository Structure

### `system/`
Core definitions that govern everything else. Change nothing here without following the change-control process.
- `architecture/` — this document and related design records
- `governance/` — ownership, review cadences, change control
- `taxonomies/` — all controlled vocabularies (enums, statuses, categories)
- `schemas/` — Notion database schemas and content frontmatter schema
- `standards/` — naming conventions, data quality rules, citation standards, ID registry

### `processes/`
Canonical documentation of every Cyprus administrative process we advise on. Each document follows the process template and carries a status, confidence level, and source type.

### `sops/`
Standard Operating Procedures for internal team operations. These tell the team *how to do things* — they are the operational complement to the process docs (which document *how Cyprus bureaucracy works*).

### `knowledge/`
Structured reference knowledge, separated by source type:
- `official/` — summaries of official government guidance
- `field/` — practical intelligence from partners and real-world experience
- `faqs/` — canonical answers to frequently asked questions
- `decision-trees/` — logic trees for routing clients to the right process

### `content-system/`
Everything governing what and how we publish:
- `strategy/` — content strategy, audience needs, gap analysis
- `style-guide/` — tone, voice, editorial standards, legal disclaimers
- `content-types/` — definitions for each type of content we produce
- `topical-map/` — pillar and cluster structure for topical authority
- `templates/` — page-level templates for content production
- `rules/` — SEO, linking, update cadence, accuracy rules

### `partners/`
All partner system definitions:
- `onboarding/` — how to bring on a new partner
- `categories/` — definitions and criteria for each partner category
- `service-catalogue/` — what services partners offer and how they are classified
- `referral-rules/` — eligibility, routing logic, disclosure requirements
- `_templates/` — partner profile and agreement templates

### `icps/`
Ideal Client Profile system:
- `framework/` — the segmentation model and scoring criteria
- `segments/` — one file per segment with full profile
- `mapping/` — how each ICP maps to services and content

### `workflows/`
Lifecycle definitions for each operational pipeline. These define states, transitions, and triggers — not step-by-step instructions (that is what SOPs are for).

### `prompts/`
AI prompt library. Prompts are version-controlled here and referenced in SOPs.

### `research/`
Research infrastructure — frameworks for how to research topics, source registry, validation checklists.

### `assets/`
Raw inputs — interview transcripts, research session captures. Never edited; only added to.

---

## Tool Stack

See [system/architecture/tool-stack.md](tool-stack.md) for the full tool inventory and integration map.

---

## Key Design Decisions

See [system/architecture/decision-log.md](decision-log.md) for the architecture decision record.
