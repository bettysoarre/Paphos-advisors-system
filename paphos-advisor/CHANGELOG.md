# System Changelog

This file records significant system-level changes: new taxonomy values, schema changes, governance updates, structural additions. It is not a git commit log — it captures *why* changes were made, not just what changed.

For process document changes, see the `updated` and `field_notes` frontmatter within each process file.

---

## Format

```
## [YYYY-MM-DD] — Short title

**Type:** [Schema change | Taxonomy update | Structural addition | Governance update | Standards update]
**Area:** [system | processes | sops | knowledge | content-system | partners | icps | workflows]
**Author:** [name]

**What changed:** Description of the change.
**Why:** Reason for the change.
**Impact:** What needs to be updated downstream (Notion databases, templates, existing records).
```

---

## Log

## [2026-04-13] — Initial system build

**Type:** Structural addition
**Area:** All
**Author:** Jason / Betty

**What changed:** Full repository structure created. Includes taxonomies, schemas, governance, standards, templates, process documents (PROC-IMM-001, PROC-TAX-001, PROC-TAX-002, PROC-PROP-001), content type definitions, topical map, partner onboarding checklist, and prompt library.

**Why:** Initial system build for Paphos Advisors knowledge and operations platform.

**Impact:** Notion databases (Partners, Content Pipeline, Research Log, Process Library) created and linked to schemas defined in `system/schemas/`.
