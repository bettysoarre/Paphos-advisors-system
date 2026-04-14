# Versioning Strategy

## Git as the Version History

No version numbers in filenames. No `_v2`, `_final`, `_revised` suffixes. Git's commit history is the complete, auditable version record for every file in the repository. To see what a file contained at any point in time, use `git log` and `git show`.

---

## Branch Strategy

| Branch | Purpose | Who Writes | Merge Rule |
|--------|---------|------------|------------|
| `main` | Canonical, always-valid system state. Everything on main is authoritative. | Merges only — never commit directly | Requires review and deliberate merge decision |
| `drafts` | Work in progress — new process docs, SOPs, content type definitions being authored | Any contributor | Merge to main when document reaches `validated` or `active` status |
| `research-intake` | Incoming validated research captures and field intelligence before extraction into structured knowledge | Research workflow | Merge to main after knowledge extraction SOP is complete |

Additional short-lived branches may be created for specific tasks (e.g., `schema/add-case-database`, `taxonomy/update-partner-categories`) and deleted after merging.

**Rule:** Nothing on `drafts` or `research-intake` is considered authoritative. Only `main` is the system of record.

---

## Commit Message Conventions

Format: `type(scope): description`

**type** — the nature of the change

| Type | Use for |
|------|---------|
| `process` | New or updated process documentation |
| `sop` | New or updated SOP |
| `knowledge` | New or updated knowledge article, FAQ, or decision tree |
| `schema` | New or updated Notion database schema |
| `taxonomy` | New or updated taxonomy file |
| `content-system` | Content type definitions, style guide, strategy docs |
| `workflow` | Workflow definition changes |
| `prompt` | New or updated AI prompt |
| `icp` | ICP segment or framework changes |
| `partners` | Partner category, service catalogue, referral rules |
| `system` | Architecture, governance, standards |
| `fix` | Correction to existing content (factual error, broken link, etc.) |
| `chore` | Housekeeping (renaming, moving files, formatting) |

**scope** — the subfolder or domain affected (e.g., `immigration`, `content`, `notion-schemas`)

**description** — imperative present tense, lowercase, no period

Examples:

```
process(immigration): add yellow slip eu national procedure
taxonomy(process-status): add needs-revalidation state with transition rules
schema(notion): add partner database schema with referral fields
fix(immigration): correct document list for pink slip application
sop(research): add source validation checklist step
chore: rename ys-eu.md to yellow-slip-eu-national.md per naming conventions
```

---

## When to Tag Releases

Git tags mark significant system milestones. Use semantic versioning: `vMAJOR.MINOR`.

Create a tag when:

- **MAJOR increment:** Taxonomy breaking change (removing or renaming a value), schema change that requires Notion database migration, significant architecture restructure
- **MINOR increment:** New top-level section added, significant new process domain added, major style guide revision

Tags are created only on `main`. Tag format: `v1.0`, `v1.1`, `v2.0`.

---

## CHANGELOG.md

`CHANGELOG.md` is updated for every tagged release and for any change that has operational consequences (e.g., a taxonomy value rename that requires updating Notion records). It is not a commit log — it summarises meaningful changes for team members who need to know what changed without reading every commit.

Format:

```
## [v1.1] — 2026-06-01

### Added
- Complete immigration process documentation for EU nationals (PROC-IMM-001 to PROC-IMM-004)
- Residency route selector decision tree (DT-RES-001)

### Changed
- Partner status taxonomy: added `paused` value (TAX-PART-001)

### Fixed
- Yellow slip document list: corrected passport copy requirement

## [v1.0] — 2026-04-01

Initial system architecture. All top-level folders and core schemas established.
```
