# Content Pipeline — Lifecycle

## Purpose
Defines the lifecycle of a content item from idea through to published and maintained. This is the workflow definition — the day-to-day procedures are in `sops/content/`.

---

## States

```
Idea → Briefed → In Production → In Review → Approved → [Scheduled →] Published → Needs Update → [Published again] / [Archived]
                      ↓                ↓
                   Blocked          Blocked
```

| State | Meaning | Who acts next |
|---|---|---|
| Idea | Content topic identified, not yet briefed | Content lead |
| Briefed | Brief created in Notion, pending writer assignment | Content lead |
| In Production | Writer actively working on the draft | Writer |
| In Review | Draft submitted for editorial review | Reviewer |
| Approved | Review passed, ready to publish or schedule | Publisher |
| Scheduled | Approved and queued for a future publish date | CMS / Publisher |
| Published | Live on website | Monitor |
| Needs Update | Published content flagged for update | Content lead |
| Blocked | Cannot progress — reason must be noted in Notion | Content lead |
| Archived | Retired content, no longer live | No action needed |

---

## Transitions

| From | To | Trigger |
|---|---|---|
| Idea | Briefed | Content lead creates brief in Notion |
| Briefed | In Production | Writer assigned and due date set |
| Briefed | Blocked | Source material unavailable or research not complete |
| In Production | In Review | Writer completes draft (see SOP-CON-001) |
| In Production | Blocked | Blocker identified mid-draft |
| In Review | Approved | Reviewer approves (see SOP-CON-002) |
| In Review | In Production | Reviewer returns for revision |
| Approved | Scheduled | Publish date set in CMS |
| Approved | Published | Publisher goes live immediately (see SOP-CON-003) |
| Scheduled | Published | Scheduled date reached |
| Published | Needs Update | Review date reached, regulatory change, or quality flag |
| Needs Update | In Production | Major update required |
| Needs Update | Published | Minor update made directly |
| Blocked | Briefed | Blocker resolved, brief still valid |
| Blocked | In Production | Blocker resolved, draft already started |
| Published | Archived | Content retired (see SOP-CON-004) |

---

## SLA Guidelines

| Transition | Target time |
|---|---|
| Brief → In Production assignment | 3 business days |
| In Production → Review submission | Per brief due date |
| Review → Decision (approve/return) | 3 business days |
| Approved → Published | 2 business days |
| Needs Update → Action | Per urgency (see SOP-CON-004) |

---

## Blockers

A content item can be blocked when:
- Source material (process doc) not yet at `validated` status
- Keyword research not completed
- Writer unavailable

Blocked items must have a reason noted in Notion and a target unblock date.
