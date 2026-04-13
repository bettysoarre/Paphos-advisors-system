# Case Pipeline — Lifecycle

## Purpose
Defines the lifecycle of a client case from initial enquiry through to closure. Procedures are in `sops/cases/`.

---

## States

```
Enquiry → Assessment → Proposal Sent → Active → [On Hold] / Closed (Won or Lost)
```

| State | Meaning |
|---|---|
| Enquiry | Initial contact received, not yet assessed |
| Assessment | Client needs and fit being evaluated |
| Proposal Sent | Service scope and fee sent to client |
| Active | Engagement confirmed, case in progress |
| On Hold | Client has paused engagement |
| Closed — Won | Case successfully completed |
| Closed — Lost | Client did not proceed |

---

## Transitions

| From | To | Trigger |
|---|---|---|
| Enquiry | Assessment | Initial contact responded to |
| Assessment | Proposal Sent | Client assessed as a fit — scope agreed |
| Assessment | Closed — Lost | Client assessed as not a fit, or client does not engage after assessment |
| Proposal Sent | Active | Client confirms engagement |
| Proposal Sent | Closed — Lost | Client declines or does not respond after 2 follow-ups |
| Active | On Hold | Client requests pause |
| On Hold | Active | Client resumes |
| On Hold | Closed — Lost | Client does not resume after agreed hold period |
| Active | Closed — Won | All deliverables complete — see SOP-CAS-004 |
| Active | Closed — Lost | Client withdraws mid-engagement |

---

## Priority Levels

| Level | When to use |
|---|---|
| High | Hard deadline (visa expiry, property completion, tax filing), or complaint |
| Normal | Default for all active cases |
| Low | On hold, or early stage with no immediate actions |

---

## Case Health Indicators

A case is considered healthy when:
- Next action and due date are always set
- Last client contact was within 7 days
- No overdue actions

A case is flagged for review when:
- No client contact for 14+ days on an active case
- Next action date is overdue
- Client has raised a concern
