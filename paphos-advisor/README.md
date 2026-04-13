# Paphos Advisors — Knowledge & Operations System

## What This Is

This repository is the source of truth for how Paphos Advisors operates. It contains:

- **Process documentation** — step-by-step records of every Cyprus administrative process we advise on
- **Standard Operating Procedures** — how our team handles content, partners, cases, and research
- **Knowledge base** — structured intelligence from official sources and field experience
- **Content system** — the architecture, rules, and templates governing everything we publish
- **Partner system** — definitions, onboarding procedures, and referral logic
- **ICP framework** — ideal client profiles and how we serve each segment
- **Workflows** — lifecycle definitions for every operational pipeline
- **Prompts** — AI prompt library for research, content, and knowledge extraction

Notion is the operational frontend for day-to-day use. This repository is the canonical definition layer — everything in Notion is derived from what is defined here.

---

## Quick Start for New Team Members

### 1. Understand the system
Read [ARCHITECTURE.md](ARCHITECTURE.md) — it explains how the pieces fit together and which tool to use for what.

### 2. Understand the naming conventions
Read [system/standards/naming-conventions.md](system/standards/naming-conventions.md) before creating or editing any files.

### 3. Find what you need
| I want to... | Go to... |
|---|---|
| Look up a process (e.g. Yellow Slip) | `processes/immigration/` |
| Find out how to handle a case | `sops/cases/` |
| Onboard a new partner | `partners/onboarding/` + `sops/partners/` |
| Write a piece of content | `content-system/` |
| Run a research session | `prompts/research/` + `sops/research/` |
| Understand a client segment | `icps/segments/` |
| Extract knowledge from an interview | `prompts/extraction/interview-extraction-prompt.md` |

### 4. Understand the review cadences
Read [system/governance/review-cadences.md](system/governance/review-cadences.md) to know when things need to be updated.

---

## Folder Map

```
paphos-advisor/
├── system/          Core definitions — taxonomies, schemas, standards, governance
├── processes/       Canonical process documentation by area
├── sops/            Internal operating procedures
├── knowledge/       Reference knowledge — official, field, FAQs, decision trees
├── content-system/  Content architecture, rules, templates, topical map
├── partners/        Partner definitions, onboarding, referral rules
├── icps/            Ideal client profiles and mapping
├── workflows/       Lifecycle definitions for each operational pipeline
├── prompts/         AI prompt library
├── research/        Research frameworks, source registry, validation checklists
└── assets/          Transcripts, research captures, archive
```

---

## Key Principles

- **GitHub is the source of truth.** If it is not in this repo, it is not canonical.
- **Notion is the working layer.** Use it for day-to-day operations, but decisions and definitions live here.
- **Every record has an ID.** See [system/standards/id-registry.md](system/standards/id-registry.md).
- **Confidence levels matter.** Never present unverified information to clients without flagging it.
- **Review cadences are mandatory.** Stale process docs cause real harm.

---

## Governance

Owner: Jason (all domains until roles are hired)
Review: See [system/governance/review-cadences.md](system/governance/review-cadences.md)
Changes: See [system/governance/change-control.md](system/governance/change-control.md)
