---
title: Notion Content Pipeline — Automations Specification
type: workflow-spec
status: ready-to-configure
created: 2026-04-25
updated: 2026-04-25
owner: lead-advisor
database: Content Pipeline (b8429a09-8cef-4fdf-aafc-82b990db0689)
---

# Notion Automations — Content Pipeline

Specification for all automations to configure in the Notion Content Pipeline database. Configure each automation via: Content Pipeline database → ⚡ Automations → + New automation.

All automations are internal to Notion. None trigger external systems (website, GitHub, email) — those require a separate integration once the website platform is confirmed.

---

## Automation 1: Set Published Date on Publication

**Trigger:** Status is changed to `published`
**Action:** Set `Published Date` property to today's date

**Why:** Prevents the publisher from forgetting to record the publish date. The Published Date field is required for calculating review schedules.

**Notion setup:**
- Trigger: Property changed → Status → is → published
- Action: Edit property → Published Date → Set to → Today

---

## Automation 2: Notify on In Review

**Trigger:** Status is changed to `in-review`
**Action:** Notify the person assigned in `Assigned To`

**Why:** Reviewer needs to know a draft is waiting for them without the writer having to send a separate message.

**Notion setup:**
- Trigger: Property changed → Status → is → in-review
- Action: Send notification to → Assigned To (property)
- Message: "A draft is ready for your review: {Title}"

---

## Automation 3: Notify on Approved

**Trigger:** Status is changed to `approved`
**Action:** Notify the person assigned in `Assigned To`

**Why:** Publisher needs to know content is cleared for publication.

**Notion setup:**
- Trigger: Property changed → Status → is → approved
- Action: Send notification to → Assigned To (property)
- Message: "{Title} has been approved and is ready to publish."

---

## Automation 4: Set Next Review Date on Publication

**Trigger:** Status is changed to `published`
**Action:** Set `Next Review Date` to 6 months from today

**Why:** Every published piece needs a scheduled review. Six months is the default; the publisher can adjust manually for evergreen content (12 months) or volatile regulatory content (3 months).

**Notion setup:**
- Trigger: Property changed → Status → is → published
- Action: Edit property → Next Review Date → Set to → Today + 6 months

*Note: Adjust to 12 months or 3 months manually after the automation runs, based on content volatility.*

---

## Automation 5: Flag Overdue In-Production Items

**Trigger:** Due Date is reached AND Status is `in-production`
**Action:** Notify Assigned To

**Why:** Catches drafts that have gone past their due date without being submitted for review.

**Notion setup:**
- Trigger: Date reached → Due Date
- Condition: Status is in-production
- Action: Send notification to → Assigned To (property)
- Message: "{Title} is past its due date and is still in production."

---

## Automation 6: Flag Needs-Update Items for Action

**Trigger:** Status is changed to `needs-update`
**Action:** Notify Assigned To

**Why:** The content lead needs to decide whether this is a major update (→ in-production) or a minor fix (→ publisher handles directly).

**Notion setup:**
- Trigger: Property changed → Status → is → needs-update
- Action: Send notification to → Assigned To (property)
- Message: "{Title} has been flagged for update. Review and route to in-production or fix directly."

---

## Automations NOT to configure yet

These automations require the website platform to be confirmed before they can be set up:

| Automation | Requires |
|---|---|
| Trigger website publish on status → approved | CMS webhook or API |
| Trigger Google Search Console index request | Search Console API integration |
| Sync Markdown from GitHub to Notion page body | GitHub + Notion integration (Make, Zapier, or custom) |

---

## Validation Steps After Configuration

After setting up all six automations, test by:

1. Create a test content record with Status = `idea`
2. Change Status to `in-production` — confirm no spurious notifications fire
3. Change Status to `in-review` — confirm Assigned To receives notification
4. Change Status to `approved` — confirm Assigned To receives notification
5. Change Status to `published` — confirm Published Date and Next Review Date are both set automatically
6. Set Due Date to yesterday, Status to `in-production` — confirm overdue notification fires

Delete the test record after validation.
