# Review Cadences

This document defines how often each record type in the Paphos Advisor system must be reviewed for accuracy, relevance, and completeness. Reviews are not optional — outdated information causes client harm and reputational risk.

---

## Summary Table

| Record Type | Default Cadence | Trigger for Earlier Review |
|-------------|----------------|---------------------------|
| Process documents | Every 6 months | Regulatory change, client issue, field flag |
| Partner records | Every 3 months | Complaint, no contact, service change |
| Knowledge articles — High confidence | Every 12 months | Regulatory change |
| Knowledge articles — Medium confidence | Every 6 months | Any contradictory source found |
| Knowledge articles — Low/Unverified | Every 3 months | Until upgraded or removed |
| Published content — Evergreen | Every 12 months | Process change, SEO drop |
| Published content — Volatile | Every 3 months | Fee or policy change |
| Taxonomies | Every 12 months | New service area or ICP segment added |
| SOPs | Every 3–12 months | See per-area rules below |
| Partner referral agreements | Every 12 months | Dispute, rate change, partner status change |

---

## 1. Process Documents

**Default cadence: Every 6 months**

Process documents govern the advice we give clients. Incorrect or outdated process information is a direct liability.

**Cadence rules:**
- All validated or published process documents must be reviewed within 6 months of their last validation date.
- High-volatility processes (fees, quotas, officer practices) should be reviewed quarterly.
- Any process document flagged as `needs-revalidation` must be reviewed within 30 days of being flagged.
- A process that has not been reviewed within 9 months must be automatically downgraded to `needs-revalidation`.

**What to check on review:**
- Have fees, timelines, or document requirements changed?
- Has the responsible government department changed its procedure or portal?
- Are there new field notes or client case outcomes to incorporate?
- Has the confidence level changed based on new evidence?

**High-volatility process areas (quarterly review recommended):**
- Immigration fees and quota rules
- Tax thresholds and filing deadlines
- Property transfer taxes and stamp duties
- Vehicle import duties and registration fees

---

## 2. Partner Records

**Default cadence: Every 3 months**

Partner records must stay current to ensure we are only referring clients to active, high-quality partners.

**Cadence rules:**
- All active partner records must be reviewed every 3 months.
- Inactive and paused partners must be reviewed every 6 months to determine whether to reactivate or remove.
- Any partner with a quality rating of `under-review` must be assessed within 14 days.

**What to check on review:**
- Is the partner still active and contactable?
- Have their services, fees, or specialisations changed?
- Have there been any client complaints or issues since the last review?
- Is their quality rating still accurate?
- Has the referral agreement or commission arrangement changed?
- Is the next review date set correctly?

---

## 3. Knowledge Articles

Review cadence is tied to the confidence level of the article.

| Confidence Level | Review Cadence |
|-----------------|----------------|
| High | Every 12 months |
| Medium | Every 6 months |
| Low | Every 3 months |
| Unverified | Every 3 months — until upgraded to Low or above, or removed |

**Additional triggers for immediate review:**
- A contradictory source is identified
- A linked process document is updated
- A client case surfaces a discrepancy
- A regulatory change is announced in a relevant area

**What to check on review:**
- Is the source still accessible and unchanged?
- Has the rule, threshold, or procedure been updated?
- Are there new field notes to add?
- Should the confidence level be upgraded or downgraded?
- Does the validation history need a new entry?

---

## 4. Published Content

Content review cadence depends on whether the content is evergreen or volatile.

### Evergreen Content
**Cadence: Every 12 months**

Evergreen content covers stable topics where the core information rarely changes. Examples: guides to the property buying process, explanations of non-dom status, ICP-oriented introductory guides.

**What to check:**
- Are all internal links still valid?
- Has the underlying process or knowledge changed?
- Are statistics, fees, or timelines still accurate?
- Is the SEO performance still acceptable, or does the content need refreshing?

### Volatile Content
**Cadence: Every 3 months**

Volatile content covers topics where key facts change frequently. Examples: content citing specific fees, visa quotas, processing times, or government portal instructions.

**What to check:**
- Have any cited fees, deadlines, or thresholds changed?
- Has the government portal or application process changed?
- Are all external links still live and pointing to current pages?

**Trigger for immediate review:**
- A regulatory change is announced
- A reader or client flags incorrect information
- The linked process document is updated

---

## 5. Taxonomies

**Cadence: Every 12 months**

Taxonomies are the controlled vocabularies that govern the entire system. They should be stable — frequent changes create inconsistency across all records that use them.

**When to trigger an out-of-cycle review:**
- A new service area is added to the advisory offering
- A new ICP segment is identified
- A new content type is introduced
- A partner category no longer reflects the network

**What to check on annual review:**
- Are all existing values still in use and accurately defined?
- Are there values that should be deprecated or merged?
- Are there new values needed to reflect current operations?
- Are all taxonomy values consistent with how they are used in Notion databases?

---

## 6. Standard Operating Procedures (SOPs)

SOP review cadence varies by area.

| SOP Area | Review Cadence |
|----------|---------------|
| Content | Quarterly |
| Partners | Quarterly |
| Cases | Quarterly |
| Research | Bi-annually |
| Knowledge | Bi-annually |
| Operations | Annually |

**What to check on SOP review:**
- Does the procedure still reflect how the work is actually done?
- Have any tools, systems, or templates referenced in the SOP changed?
- Are the outputs and handoffs still correct?
- Does the owner need to be updated?

---

## 7. Referral Agreements

**Cadence: Every 12 months**

Formal referral agreements with partners must be reviewed annually to ensure terms remain current and agreed.

**Trigger for immediate review:**
- A partner disputes a referral or commission payment
- A partner's services or pricing change significantly
- A partner's status changes to paused, inactive, or blacklisted

---

## Enforcement

- Review dates are tracked via the `Next Review Date` field in each Notion database.
- The system owner (see `ownership-matrix.md`) is responsible for ensuring reviews happen on schedule.
- A weekly Notion view filtered by `Next Review Date ≤ today + 14 days` should be monitored as a standing agenda item.
- Missed reviews must be logged with a reason and rescheduled immediately — they cannot simply be skipped.
