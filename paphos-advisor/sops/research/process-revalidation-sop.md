---
id: SOP-RES-004
title: Process Revalidation SOP
area: research
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-RES-001, SOP-RES-002, SOP-RES-003]
---

# Process Revalidation SOP

## Purpose
Defines how to revalidate a process document when it reaches its review date or when a change is suspected.

## When to Use
- A process doc reaches its `next_review_due` date
- A regulatory change is announced (budget, legislation update, government announcement)
- A partner flags that a process has changed
- A client case reveals a discrepancy between the doc and reality

---

## Steps

### 1. Identify what needs checking
Before running research, review the process doc and identify:
- Which specific steps or facts are most likely to have changed
- What the open questions were from the last review
- Whether any partner has recently mentioned changes in this area

### 2. Check official sources first
Go to the official sources listed in the process doc. Check:
- Has the page content changed?
- Is there a new version of the relevant legislation or guidance?
- Has the government announced any changes?

Use `prompts/research/regulatory-update-check-prompt.md` to structure this check in Perplexity.

### 3. Check with partners (for high-stakes processes)
For processes where field intelligence is critical (immigration, tax), contact the relevant partner(s) to ask:
- "Have you seen any changes to [process] recently?"
- "Is the [specific step] still working the same way?"

This is a lighter touch than a full interview — a 10-minute conversation or email exchange.

### 4. Update the process doc

**No changes found:**
- Update the `updated` field in frontmatter
- Update `next_review_due`
- Add a `field_note` entry: `[date] — Revalidation check complete. No changes found. [source].`

**Changes found:**
- Update all affected sections
- Update `field_notes` to explain what changed and when
- Reassess confidence level
- If status was `validated` or `published`, set it to `needs-revalidation` until the update is reviewed
- Log the change in CHANGELOG.md if significant

### 5. Update published content
If there is published content derived from this process doc:
- Review the content for accuracy against the updated doc
- If content is now inaccurate, create a content update task in Notion (SOP-CON-004)

### 6. Notify the team
If the change affects advice being given to active cases, notify the assigned advisors immediately.

---

## Emergency Revalidation
If a regulatory change is announced that materially affects an active client:
1. Update the process doc immediately (within 24 hours)
2. Set status to `needs-revalidation`
3. Notify affected active cases
4. Do not wait for the full revalidation cycle — flag and advise on the change now, complete the full revalidation within 1 week
