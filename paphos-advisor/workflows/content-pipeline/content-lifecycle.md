# Content Pipeline — Lifecycle

## Purpose
Defines the lifecycle of a content item from idea through to published and maintained. This is the workflow definition — the day-to-day procedures are in `sops/content/`.

---

## States

```
Idea → Brief → In Production → Review → Approved → Published → Needs Update → [Published again] / [Archived]
```

| State | Meaning | Who acts next |
|---|---|---|
| Idea | Content topic identified, not yet briefed | Content lead |
| Brief | Brief created in Notion, pending assignment | Content lead |
| In Production | Writer is actively working on the draft | Writer |
| Review | Draft submitted for editorial review | Reviewer |
| Approved | Review passed, ready to publish | Publisher |
| Published | Live on website | Monitor |
| Needs Update | Published content flagged for update | Content lead |
| Archived | Retired content, no longer live | No action needed |

---

## Transitions

| From | To | Trigger |
|---|---|---|
| Idea | Brief | Content lead decides to progress |
| Brief | In Production | Writer assigned and due date set |
| In Production | Review | Writer completes draft (see SOP-CON-001) |
| Review | Approved | Reviewer approves (see SOP-CON-002) |
| Review | In Production | Reviewer returns for revision |
| Approved | Published | Publisher goes live (see SOP-CON-003) |
| Published | Needs Update | Scheduled review date reached, regulatory change, or quality flag |
| Needs Update | In Production | Major update required |
| Needs Update | Published | Minor update made directly |
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
