---
id: SOP-PAR-004
title: Referral Tracking SOP
area: partners
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-PAR-001, SOP-PAR-003]
---

# Referral Tracking SOP

## Purpose
Defines how to record, track, and close the loop on partner referrals — both outbound (us referring a client to a partner) and inbound (a partner referring a client to us).

---

## Outbound Referrals (We Refer a Client to a Partner)

### When to make a referral
Only refer a client to a partner when:
- The client has expressed a need that falls within the partner's service area
- The partner is `active` status (not `probationary`, `suspended`, or `archived`)
- The referral is in the client's best interest (not based on commercial incentive alone)
- Disclosure requirements have been met (see `partners/referral-rules/referral-disclosure-requirements.md`)

### Steps
1. **Identify the right partner** — use the routing logic in `partners/referral-rules/referral-routing-logic.md`
2. **Check eligibility** — confirm the partner is `active` and appropriate for this client's ICP segment
3. **Disclose to the client** — inform the client that you are making a referral and the nature of any commercial relationship
4. **Make the introduction** — warm email introduction. Do not simply hand over a phone number.
5. **Log in Notion** — in the client's Case record, add the partner to `Partners Referred To` and note the date
6. **Follow up** — after 2 weeks, check in with the client to confirm the referral was received and they are proceeding

### Closing the loop
- After the client has completed their engagement with the partner, note the outcome in the Case record
- If outcome was positive: note in the partner review for their next scheduled review
- If outcome was negative: trigger a partner review (see SOP-PAR-003)

---

## Inbound Referrals (A Partner Refers a Client to Us)

### Steps
1. **Acknowledge receipt** — contact the referred prospect within 1 business day
2. **Create a Contact record** in Notion — set `How They Found Us` to `Referral — Partner` and link the referring partner
3. **Proceed through normal case intake** — follow SOP-CAS-001
4. **Notify the referring partner** — once the client has engaged, let the partner know their referral converted (builds the relationship)
5. **Track for reciprocity** — note the inbound referral in the partner's Notion record

---

## Referral Disclosure Requirements

See `partners/referral-rules/referral-disclosure-requirements.md` for the full disclosure script.

Summary:
- Always disclose the referral relationship to the client before making the referral
- If there is a commercial arrangement with the partner (referral fee or reciprocal referrals), this must be disclosed
- Do not make referrals contingent on commercial benefit to Paphos Advisors alone

---

## Record-Keeping

Every referral must be logged in the relevant Case record in Notion. Do not rely on memory or informal notes.

Minimum fields to complete:
- Partners Referred To (relation to Partners DB)
- Date of referral (in case notes)
- Outcome (when known)
