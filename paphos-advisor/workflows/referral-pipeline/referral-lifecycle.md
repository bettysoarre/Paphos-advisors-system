# Referral Pipeline — Lifecycle

## Purpose
Defines the lifecycle of an outbound referral from the decision to refer through to outcome recording. Procedures are in `sops/partners/referral-tracking-sop.md`.

---

## States

```
Pending → Introduced → Engaged → Outcome Recorded
```

| State | Meaning |
|---|---|
| Pending | Decision made to refer, introduction not yet made |
| Introduced | Warm introduction email sent to client and partner |
| Engaged | Client has confirmed they are working with the referred partner |
| Completed — Positive | Client reported positive outcome |
| Completed — Negative | Client reported poor outcome or complaint |
| No Response | Client did not follow up on the referral |

---

## Transitions

| From | To | Trigger |
|---|---|---|
| Pending | Introduced | Introduction email sent |
| Introduced | Engaged | Client confirms they have engaged the partner |
| Introduced | No Response | 2 weeks with no client update |
| Engaged | Completed — Positive | Client reports positive outcome |
| Engaged | Completed — Negative | Client reports issue with partner |
| No Response | Completed — No Response | Closed without outcome |

---

## Notes

All referral events must be logged in the Case record in Notion under `Partners Referred To` and in the case notes.

Completed — Negative outcomes trigger an automatic partner review (see SOP-PAR-003).
