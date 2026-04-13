# Research Pipeline — Lifecycle

## Purpose
Defines the lifecycle of a research session from planning through to knowledge integration. Procedures are in `sops/research/`.

---

## States

```
Planned → In Progress → Captured → Extracting → Integrated
```

| State | Meaning |
|---|---|
| Planned | Research session identified and scoped, not yet run |
| In Progress | Research session actively being conducted |
| Captured | Session complete, output saved to assets/research-captures/ |
| Extracting | Extraction prompt running against the captured output |
| Integrated | Knowledge extracted, KB articles created, process docs updated |

---

## Transitions

| From | To | Trigger |
|---|---|---|
| Planned | In Progress | Research session started |
| In Progress | Captured | Session complete and output saved (SOP-RES-001) |
| Captured | Extracting | Extraction prompt run against output |
| Extracting | Integrated | KB articles created, process docs updated (SOP-RES-003) |

---

## Notes

- Every research session must create a Research Log entry in Notion before it begins (status: Planned)
- Sessions should not be marked Integrated until the downstream process docs have actually been updated — not just the KB articles created
- A session may produce multiple KB articles across different topic areas; all must be created before marking Integrated
