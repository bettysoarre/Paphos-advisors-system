# Content Type: Partner Profile

## Definition
A brief, factual profile of a vetted partner published on the website. Designed to give prospective clients confidence in the partners we refer them to, and to give partners a benefit from the relationship.

## Eligibility
Only `active` partners (trust level: `trusted` or above) are eligible for a published profile. `Probationary` partners are not published until the 90-day review is complete.

## Word count
300–500 words

## Required sections

1. **Partner name and category** — visible in the page title and H1
2. **Services offered** — bullet list of specific services (from the partner's service catalogue entry)
3. **Areas of expertise** — which Cyprus processes they specialise in
4. **Languages** — languages spoken (important for international clients)
5. **Location and service area** — Paphos, island-wide, remote, etc.
6. **Brief description** — 2-3 sentences about the firm/individual. Written in third person. Not promotional — factual.
7. **Disclosure notice** — referral relationship disclosure (mandatory — see `legal-disclaimer-rules.md`)
8. **How to enquire** — contact method or CTA to contact us for a referral

## What is NOT included

- Partner's personal biography (not relevant to clients)
- Fee information (too variable; handle in referral conversation)
- Client testimonials attributed to specific clients (privacy)
- Rankings or "best" claims ("Paphos's top immigration lawyer")
- Anything the partner has not approved for publication

## Process

Before publishing, the partner must:
1. Review the draft profile
2. Confirm all information is accurate
3. Approve publication in writing

Do not publish partner profiles without explicit approval.

## SEO requirements

| Element | Requirement |
|---|---|
| Meta title | "[Partner name] — [Category] in Paphos, Cyprus" |
| Structured data | LocalBusiness schema |
| Index | Yes (partner profiles are indexable content) |

## LocalBusiness Schema (minimal)

```json
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "name": "[Partner firm name]",
  "description": "[Brief description]",
  "areaServed": "Paphos, Cyprus",
  "knowsAbout": ["Cyprus immigration law", "MEU1 applications"]
}
```

## Update cadence
Every 3 months (aligned with partner review cadence). If a partner's status changes (suspended, archived), the profile must be unpublished immediately — do not leave live profiles for inactive partners.

## Partner profile template
See `partners/_templates/partner-profile-template.md` for the source-of-truth template used to draft profiles.
