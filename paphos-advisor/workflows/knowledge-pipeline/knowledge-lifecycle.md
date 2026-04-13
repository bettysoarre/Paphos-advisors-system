# Knowledge Pipeline — Lifecycle

## Purpose
Defines the lifecycle of a knowledge article from creation through to validation and eventual retirement. Procedures are in `sops/knowledge/`.

---

## States

```
Draft → Review → Validated → [Needs Revalidation → Review again] / [Archived]
```

| State | Meaning |
|---|---|
| Draft | KB article created, not yet reviewed for accuracy |
| Review | Under review for accuracy, completeness, and source quality |
| Validated | Reviewed and approved. Safe to reference in content and advice. |
| Needs Revalidation | Previously validated but circumstances have changed |
| Archived | No longer current. Kept for historical reference. |

---

## Transitions

| From | To | Trigger |
|---|---|---|
| Draft | Review | Article created and ready for review |
| Review | Validated | Review passed — confidence level is medium or higher |
| Review | Draft | Review returns for revision (incomplete, poor sources, low confidence) |
| Validated | Needs Revalidation | Review cadence reached, or change detected |
| Needs Revalidation | Review | Revalidation research complete, ready for review |
| Validated | Archived | Article retired per SOP-KNW-003 |
| Needs Revalidation | Archived | Article cannot be revalidated (process no longer exists, etc.) |

---

## Review Cadences

| Confidence level | Review cycle |
|---|---|
| High | 12 months |
| Medium | 6 months |
| Low | 3 months |
| Unverified | As soon as possible — should not remain unverified indefinitely |
