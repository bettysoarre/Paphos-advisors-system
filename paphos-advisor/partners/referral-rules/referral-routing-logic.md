# Referral Routing Logic

## Purpose
Defines how to determine which partner to refer a client to, given the client's ICP segment and the service they need.

---

## Routing Decision Process

### Step 1: Identify the service needed
From the Case record, identify which specific services the client needs. Use the service types from `partners/service-catalogue/service-types-overview.md`.

### Step 2: Identify eligible partners
Filter the Notion Partners database:
- Category = [relevant category]
- Status = Active
- Services Offered includes [specific service]
- Trust level = Trusted (or Probationary with approval)

### Step 3: Select the best match
If multiple eligible partners exist, select based on:

| Factor | Guidance |
|---|---|
| ICP segment alignment | Does this partner have experience with clients like this? (check their Notion record notes) |
| Language | Does the client speak a language this partner covers? |
| Capacity | Has the partner indicated they have capacity? |
| Recent performance | Check most recent client outcomes for this partner |
| Relationship | For high-value clients, has Jason personally worked with this partner? |

### Step 4: Document and refer
Follow SOP-PAR-004 (Referral Tracking SOP) for the mechanics of making the referral.

---

## ICP-to-Partner-Category Routing Matrix

| ICP Segment | Primary partner category | Secondary (where applicable) |
|---|---|---|
| EU National — Remote Worker | Immigration Lawyers (MEU1), Tax Advisors (Non-Dom, 60-day) | Property Agents (rental) |
| UK National — Retiree | Immigration Lawyers (Category F), Financial Advisors (pensions) | Healthcare Providers, Property Agents |
| Non-EU Digital Nomad | Immigration Lawyers (Digital Nomad Visa) | Tax Advisors (if seeking tax residency) |
| Entrepreneur — Company Formation | Tax Advisors (corporate), Immigration Lawyers (if director needs residency) | Financial Advisors (wealth structuring) |
| HNI — Permanent Residency | Immigration Lawyers (Category 6.2), Property Agents (€300k property) | Financial Advisors, Tax Advisors |
| Family Relocating with Children | Immigration Lawyers (family MEU1), Property Agents (family rental) | Healthcare Providers, Removal Companies |

---

## Routing When No Partner is Available

If no eligible partner exists in the required category:
1. Be transparent with the client — do not pretend you have a partner
2. Offer to help them find one (advise on what to look for, what to verify)
3. Log the gap in the Notion Research Log — this is an active partner acquisition need
4. Prioritise finding a partner in this category

Do not refer to a partner who has not been vetted simply to fill the gap.

---

## Multiple Partners for the Same Client

A client often needs multiple partner types simultaneously (e.g., immigration lawyer + tax advisor + property agent). Each referral follows the same routing logic independently. Coordinate introductions so the client is not overwhelmed — consider sequencing if appropriate:

Typical sequence for EU Remote Worker:
1. Property Agent → rental to establish address
2. Immigration Lawyer → Yellow Slip (requires address)
3. Tax Advisor → tax residency (requires Yellow Slip or at least TIC)
