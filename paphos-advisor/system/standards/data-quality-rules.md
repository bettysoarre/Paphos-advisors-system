# Data Quality Rules

## Purpose

This document defines what makes a record complete and valid in the Paphos Advisors system. These rules apply to process documents, KB articles, partner records, and content briefs. A record that does not meet these standards should not move to the next status.

---

## Process Documents

### Minimum requirements to move from `stub` to `draft`
- [ ] `id` field populated (format: PROC-[AREA]-[NNN])
- [ ] `title` is descriptive and follows naming conventions
- [ ] `area` and `sub_area` fields populated with taxonomy values
- [ ] `status` set to `draft`
- [ ] `confidence` set (even if `unverified`)
- [ ] `source_type` set
- [ ] At least one of: official source URL, research session reference, or partner interview reference
- [ ] Overview section written (even if brief)

### Minimum requirements to move from `draft` to `in-research`
All of the above, plus:
- [ ] Key steps section has at least a skeleton of the process
- [ ] Known open questions documented in `field_notes`
- [ ] Research session or official source referenced

### Minimum requirements to move from `in-research` to `review`
All of the above, plus:
- [ ] All major sections of the process template completed
- [ ] Documents required listed with specifics (not just "proof of identity")
- [ ] Real-world processing time noted (not just official time) where known
- [ ] Cost estimates included where applicable
- [ ] At least one field note entry with source

### Minimum requirements to move from `review` to `validated`
All of the above, plus:
- [ ] Confidence level is `medium` or `high` (not `low` or `unverified`)
- [ ] At least one field source or official source corroborating the key steps
- [ ] Open questions either resolved or explicitly flagged as unresolved
- [ ] `reviewed_by` and `review_date` populated

### Minimum requirements to move from `validated` to `published`
All of the above, plus:
- [ ] Content has been derived from this doc (or decision made not to publish content yet)
- [ ] Notion Process Library record updated
- [ ] `published_date` populated

---

## Knowledge Articles

### Minimum requirements to be created
- [ ] `id` field populated (format: KB-[TYPE]-[NNN])
- [ ] `title` is a clear, specific claim (not vague)
- [ ] `source_type` set
- [ ] `confidence` set
- [ ] `source` references the interview, session, or document it came from
- [ ] Body contains the actual knowledge claim (not just a placeholder)

### Minimum requirements to be referenced in content
- [ ] Confidence is `medium` or `high`
- [ ] Source is traceable (not just "general knowledge")
- [ ] If `field` source: at least one partner interview or observation supporting it

---

## Partner Records (Notion)

### Minimum requirements to be `onboarded` status
- [ ] Company name, contact name, contact email populated
- [ ] Partner category set (from taxonomy)
- [ ] Services offered listed
- [ ] At least one process area tagged
- [ ] Trust level set (minimum: `probationary`)
- [ ] Commercial terms documented
- [ ] Contract on file: Yes
- [ ] Date onboarded populated

### Minimum requirements to be `active` status
All of the above, plus:
- [ ] Knowledge interview completed (Stage 4 of onboarding checklist)
- [ ] At least one KB article or process doc update attributed to this partner
- [ ] Referral workflow confirmed (they know how to receive referrals)
- [ ] 90-day review scheduled

---

## Content Briefs (Notion / Content Pipeline)

### Minimum requirements to move to `in-production`
- [ ] Title confirmed (target keyword identified)
- [ ] Content type set
- [ ] Target ICP(s) identified
- [ ] Related process doc(s) linked (if applicable)
- [ ] Word count target set
- [ ] Assigned writer/owner
- [ ] Due date set

### Minimum requirements to move to `review`
All of the above, plus:
- [ ] Draft written and meets word count
- [ ] All required sections present per content type definition
- [ ] Sources cited (not just internal knowledge)
- [ ] Disclaimer included if confidence of source material is low/medium

### Minimum requirements to move to `published`
All of the above, plus:
- [ ] Editorial review completed
- [ ] SEO requirements met (meta title, meta description, headers)
- [ ] Internal links added
- [ ] Legal disclaimer reviewed
- [ ] Published URL recorded in Notion

---

## General Rules

**No orphan IDs.** Every record with an ID must be registered in [id-registry.md](id-registry.md).

**No vague sources.** "General knowledge" or "common practice" are not acceptable sources. Cite the interview date, the research session reference, or the official URL.

**No silent demotions.** If a record's confidence level drops (e.g., because a regulation changed), update the status too. Do not leave a `validated` record with `unverified` information.

**No silent gaps.** If a required field cannot be completed, add a `TODO:` comment explaining why, rather than leaving it blank silently.
