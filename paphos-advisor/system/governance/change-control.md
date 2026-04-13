# Change Control

## Purpose

This document defines how changes are made to canonical definitions in the system — taxonomies, schemas, standards, governance rules, and process templates. It exists because uncontrolled changes to these definitions break downstream records, Notion databases, and published content.

Not all files need change control. Day-to-day additions (new process docs, new KB articles, new content briefs) do not require it. Change control applies to **structural and definitional changes only**.

---

## What Requires Change Control

| Change type | Examples | Requires change control? |
|---|---|---|
| Taxonomy value added | New status, new confidence level, new ICP segment | Yes |
| Taxonomy value renamed or removed | Renaming `validated` to `approved` | Yes |
| Schema field added | Adding a new property to the Notion Partners database | Yes |
| Schema field renamed or removed | Removing a field from the content frontmatter schema | Yes |
| Template structure changed | Adding a required section to the process template | Yes |
| Standards changed | Changing the ID format for process documents | Yes |
| Governance rule changed | Changing a review cadence | Yes |
| New process doc or KB article | Normal operational work | No |
| Content brief created or updated | Normal operational work | No |
| Partner record updated in Notion | Normal operational work | No |

---

## Change Process

### Step 1 — Identify the change
Write down:
- What is changing
- Why it is changing
- What downstream records or databases are affected

### Step 2 — Check for downstream impact
Before making the change, identify:
- Which existing files use the value/field/template being changed
- Which Notion databases need to be updated
- Whether any published content references the definition

### Step 3 — Make the change in GitHub
- Edit the relevant file in the repository
- If a taxonomy value is renamed or removed, search for all uses and update them
- If a schema changes, note which Notion database needs updating

### Step 4 — Update Notion
- Apply schema changes to the relevant Notion database
- Update any Notion views or filters that reference the changed field/value

### Step 5 — Record in CHANGELOG
Add an entry to [CHANGELOG.md](../../CHANGELOG.md) with:
- Date
- Type of change
- What changed and why
- Downstream impact

### Step 6 — Notify the team
Let affected team members know what changed and what they need to do (if anything).

---

## Who Can Make Changes

Currently all domains are owned by Jason. As the team grows, domain ownership is defined in [ownership-matrix.md](ownership-matrix.md).

The rule: **the domain owner approves changes to their domain's definitions.** Nobody edits `system/taxonomies/` or `system/schemas/` without the system owner's approval.

---

## Emergency Changes

If a process definition is found to be materially wrong (e.g., a regulation has changed), the change can be made immediately without going through the full process — but the CHANGELOG entry and downstream updates must still be done within 24 hours.

Flag emergency changes with a comment in the relevant file: `<!-- EMERGENCY UPDATE [date]: reason -->`
