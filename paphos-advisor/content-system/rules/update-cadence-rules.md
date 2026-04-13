# Update Cadence Rules

## Purpose
Defines how frequently each type of published content must be reviewed for accuracy. Stale content is a liability — it misleads users, harms SEO, and damages trust.

---

## Cadence by Content Type

| Content type | Cadence | Trigger also when... |
|---|---|---|
| Relocation guide (evergreen) | Annual | Related process doc is updated |
| Process explainer | 6 months | Related process doc is updated |
| FAQ page | 6 months | A client question reveals inaccuracy |
| Checklist | 6 months | Related process doc is updated |
| Comparison article | Annual | An option in the comparison changes |
| Partner profile | 3 months | Partner status changes in Notion |
| News update | No scheduled review | Replaced rather than updated |

---

## Triggered Reviews

In addition to the scheduled cadence, content must be reviewed immediately when:

- The underlying process doc reaches `needs-revalidation` status
- A regulation change is announced
- A client or partner reports inaccurate content
- A page's bounce rate or organic traffic drops >30% in 3 months (may indicate content is no longer meeting user intent)

---

## What "Review" Means

A review is not a full rewrite. It is a check:

1. Is every factual claim still accurate? (Check against process docs and KB articles)
2. Is the "last updated" date accurate?
3. Are all links still working?
4. Has the related process changed in a way that affects the content?
5. Are there new FAQs or user questions that should be added?

If the answer to 1-4 is yes, update accordingly. If no changes are needed, update the review date in the Notion Content Pipeline and set the next review date.

---

## Freshness Signals

Always display a "Last updated: Month YYYY" notice on:
- Process explainers
- Guides
- FAQ pages
- Checklists

This signals to users and search engines that the content is maintained. Do not display fake "updated" dates — only update this when the content actually changes.

---

## Sunset Policy

Content that cannot be kept up to date must be:
1. Clearly labelled as potentially outdated (accuracy disclaimer)
2. Scheduled for retirement or update
3. Not left in an ambiguous state where users cannot tell if it is current

If a piece has not been reviewed for twice its cadence (e.g., 12 months for a 6-month piece), treat it as stale and either update it immediately or take it offline until it can be updated.
