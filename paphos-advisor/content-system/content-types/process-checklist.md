# Content Type: Process Checklist

*Extends the base checklist rules in [`checklist.md`](checklist.md). The rules below apply additionally or override for process-linked checklists specifically.*

---

## Definition

A Process Checklist is a structured, action-oriented document that breaks a Cyprus relocation process into a sequential list of tasks the reader can follow and tick off. Each checklist is directly linked to one process document (PROC-XXX) and serves as the practical companion to it — where the process document explains the full detail, the checklist gives the reader a clean action plan.

Checklists serve three purposes:
1. **Client tool:** Given to clients at the start of a process to manage their own progress
2. **Lead magnet:** Offered as a downloadable PDF to capture email addresses
3. **Content asset:** Published on the site to capture checklist-intent search queries (e.g. "moving to Cyprus checklist")

Every checklist must be **printable, downloadable as a PDF, and self-contained** — a reader with no other context must be able to follow it.

---

## Format

### Header Block
Every checklist begins with a header block containing:
- **Process name** — the full title of the process
- **Linked process document** — ID and link to the corresponding PROC-XXX file
- **Applies to** — which ICP segments this checklist is for
- **Estimated total time** — realistic end-to-end timeline
- **Last updated** — date the checklist was last reviewed and confirmed accurate

### Phases
Checklists are divided into phases that reflect the natural stages of the process. Each phase has:
- A phase title (e.g. "Phase 1: Before You Arrive", "Phase 2: First 30 Days")
- A brief one-sentence description of what this phase covers
- A numbered list of tasks (see task format below)

**Standard phases for immigration/settling-in processes:**
1. Before You Start (preparation, documents to gather)
2. In Cyprus (actions to take in person)
3. After Submission (what to do while waiting)
4. Once Approved (next steps after completion)

**Standard phases for tax/financial processes:**
1. Establish Prerequisites (what must be in place first)
2. Gather Documentation
3. File / Register / Submit
4. Ongoing Obligations

Phases should be adapted to the specific process — not every process fits the standard structure. Use the structure that makes the steps clearest.

### Task Format

Each task is a checkbox item in this format:

```
☐  [Action verb] [specific action] — [brief context or note if needed]
```

**Rules for tasks:**
- Every task starts with an action verb (Obtain, Gather, Book, Submit, Pay, Contact, Confirm, Register, Download, Sign, etc.)
- One task = one discrete action. Do not combine two steps into one checkbox.
- Add a brief inline note (after an em dash) only where the task would be confusing without it
- Do not write explanatory paragraphs inside the checklist — keep it scannable
- If a task has a subtask (e.g. a document has specific requirements), use an indented sub-checkbox

**Example:**
```
☐  Obtain rental agreement — minimum 12-month term required
    ☐  Ensure agreement is stamped at the Tax Office before attending CRMD
☐  Gather 2 passport-sized photographs
☐  Book appointment at Paphos CRMD office — call ahead, appointments often required
```

---

## Document Requirements Section

Every checklist must include a standalone **Documents Required** section — either as a phase or as a summary box at the end. This section lists every document required for the process in a clean, scannable format.

For each document, state:
- Document name
- Format required (original / certified copy / notarised copy)
- Whether apostille is required (yes / no / sometimes)
- Whether certified Greek translation is required (yes / no / sometimes)
- Any validity restriction (e.g. "issued within last 6 months")

**Format:**

| Document | Format | Apostille | Translation | Validity |
|----------|--------|-----------|-------------|---------|
| Valid EU passport | Original + photocopy | No | No | Must be valid |
| Rental agreement | Original + photocopy | No | No | Min. 12 months |
| Bank statements | Originals or certified copies | No | Sometimes | Last 6 months |

---

## Timeline Section

Every checklist must include a **Timeline** section — a simple visual or tabular summary showing:
- Total estimated time from start to finish
- Time per phase (approximate)
- Any phase with significant variance (e.g. processing times that differ by district)

**Format:**

| Phase | Estimated Time | Notes |
|-------|---------------|-------|
| Phase 1: Preparation | 1–2 weeks | Depends on document gathering speed |
| Phase 2: Submission | 1 day | In-person appointment |
| Phase 3: Processing | 1–3 months | Paphos district; may be faster elsewhere |
| Phase 4: Post-approval | 1–2 weeks | Utility registrations, next steps |
| **Total** | **6–14 weeks** | Paphos estimate |

---

## Printable / Downloadable Requirements

Checklists must be designed for both digital use and print/PDF export.

**Requirements:**
- The checklist markdown file is the source of truth — from this, a PDF is generated for download
- PDF format: A4, clean layout, Paphos Advisors branding header, page numbers
- Checkbox items must render as actual checkboxes in PDF (not bullet points)
- Font size minimum 11pt for body text to ensure readability when printed
- Include at the bottom of the PDF: document title, version date, and the statement: *"This checklist is for guidance only. Requirements may change. Always verify with the relevant authority or a qualified advisor."*
- Do not include confidential client information in the template checklist

**File naming for downloadable PDFs:**
`[process-slug]-checklist-[YYYY-MM].pdf`
Example: `yellow-slip-eu-national-checklist-2026-04.pdf`

---

## Linked Process Document

Every checklist must be explicitly linked to its source process document. This serves two purposes:
1. It ensures the checklist is updated whenever the process document is updated
2. It allows the system to flag outdated checklists when a PROC-XXX document changes status to `needs-revalidation`

**Linking rule:** If the linked process document is updated, the checklist must be reviewed within 14 days and updated if any task, document requirement, fee, or timeline has changed.

---

## Update Cadence

| Trigger | Action |
|---------|--------|
| Linked PROC-XXX document updated | Review and update checklist within 14 days |
| Fee or timeline change | Update immediately; regenerate PDF |
| Regulatory change in process area | Review and update within 7 days |
| Scheduled review | Every 6 months regardless of triggers |

The checklist version date (shown in the PDF footer) must be updated every time the checklist is revised.

---

## Source Requirements

The checklist itself does not cite sources inline — it is an action tool, not a research document. However:

- Every task and document requirement must be traceable to the linked PROC-XXX process document
- The PROC-XXX document must be in `validated` or `published` status before its checklist is published
- Do not publish a checklist for a process that is only `draft` or `in-research` — the checklist will contain unvalidated information presented as actionable guidance

---

## Frontmatter

```yaml
---
id: CNT-CHK-[###]
title: ""                        # e.g. "Yellow Slip (MEU1) Application Checklist — EU Nationals"
content_type: checklist
linked_process: ""               # PROC-XXX ID of the source process document
target_icp:
  - ""
status: briefed
assigned_to: ""
due_date: ""
created: ""
updated: ""
pdf_filename: ""                 # e.g. yellow-slip-eu-national-checklist-2026-04.pdf
pdf_last_generated: ""           # ISO date: YYYY-MM-DD
---
```

---

## Quality Checklist (Meta)

Before a Process Checklist is marked as approved for publication:

- [ ] Linked process document is in `validated` or `published` status
- [ ] All phases are present and correctly sequenced
- [ ] Every task starts with an action verb
- [ ] Documents Required section is complete and in table format
- [ ] Timeline section is present and includes district-level variations where relevant
- [ ] PDF has been generated and reviewed for print readability
- [ ] PDF footer includes version date and disclaimer
- [ ] PDF filename follows naming convention
- [ ] Frontmatter is complete including `linked_process` and `pdf_filename`
- [ ] ICP segments are tagged correctly
