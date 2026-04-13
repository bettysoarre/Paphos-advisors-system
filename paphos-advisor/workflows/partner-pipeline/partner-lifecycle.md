# Partner Pipeline — Lifecycle

## Purpose
Defines the lifecycle of a partner relationship from identification to active status and eventual offboarding. Procedures are in `sops/partners/`.

---

## States

```
Candidate → Vetting → Contacted → Information Gathering → Interviewed → Onboarded → Active → [Suspended] / [Archived]
```

| State | Meaning |
|---|---|
| Candidate | Partner identified, vetting not yet started |
| Vetting | Stage 1 of onboarding checklist in progress |
| Contacted | First contact made, relationship building in progress |
| Information Gathering | Stage 3 of onboarding checklist in progress |
| Interviewed | Stage 4 knowledge interview complete, extraction pending |
| Onboarded | All records complete, contract on file, trust level = probationary |
| Active | Knowledge interview integrated, referral workflow confirmed |
| Under Review | Quality issue or scheduled review in progress |
| Suspended | Referrals paused pending investigation |
| Archived | Partner relationship ended |

---

## Transitions

| From | To | Trigger |
|---|---|---|
| Candidate | Vetting | Decision to assess this partner |
| Vetting | Contacted | Vetting passed — see SOP-PAR-002 |
| Vetting | Archived | Vetting failed — record rejection reason |
| Contacted | Information Gathering | Partner expresses interest |
| Information Gathering | Interviewed | Stage 4 interview scheduled and completed |
| Interviewed | Onboarded | Record completion done (Stage 6 of checklist) |
| Onboarded | Active | Knowledge extracted, referral workflow confirmed (Stage 7) |
| Active | Under Review | 90-day review, annual review, or quality flag |
| Under Review | Active | Review passed |
| Under Review | Suspended | Review reveals material issue |
| Suspended | Active | Issue resolved |
| Suspended | Archived | Issue not resolved or relationship ended |
| Active | Archived | Partner or Paphos Advisors ends relationship |

---

## Trust Levels (separate from states)

| Level | Criteria |
|---|---|
| Probationary | Newly onboarded. Limited referrals. 90-day review required. |
| Trusted | 90-day review passed. 2+ referrals with positive outcomes. No material issues. |
| Preferred | Long-term trusted partner. Priority routing for their category. |
