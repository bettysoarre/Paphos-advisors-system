---
title: Canonical URL Inventory
source: Jason's rebuilt IA workbook (paphosadvisor_rebuilt_sitemap_geo_seo.xlsx — Sitemap tab, GID 295829359) + Hierarchy/QA/ICP Notes tabs
synced: 2026-07-11
total-pages: 153
p0-count: 42
supersedes: content-system/topical-map/pillar-topics.md, previous canonical-url-inventory.md (141-page version, synced 2026-05-11 — all page IDs renumbered, do not cross-reference old P0## ids)
note: Full rebuild, not an incremental sync. All Page IDs (P001-P153) are reassigned from the previous version and do not correspond to the same pages. Full SEO metadata (title tag, meta description, secondary keywords, schema.org types, key entities, LLM retrieval angle, internal link targets, notes) is available in sitemap-full-metadata.csv in this folder. Site hierarchy (depth, nav grouping, children count) is available in site-hierarchy.csv. ICP labels now carry full descriptive names matching icps/segments/ file names — see "ICP Priority in This Sitemap" below.
---

# Canonical URL Inventory

Master reference for all pages on the Paphos Advisors website. Supersedes `pillar-topics.md`.

All content briefs, content mapping rows, and Notion Content Pipeline records derive from this file.
When Jason's sheet is updated, sync here first, then propagate changes downstream.

Full SEO metadata not captured in the table below (title tag, meta description, secondary keywords, schema type, key entities, LLM retrieval angle, internal link targets) — available in `sitemap-full-metadata.csv` in this same folder, keyed by page-id.

**Columns:** `page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status`

---

## ICP Priority in This Sitemap

| ICP | Role in this sitemap | Treatment |
|---|---|---|
| ICP-002 EU National Remote Worker | Primary design set | Top-level pathway, Yellow Slip, 60-day rule, non-dom, banking, and rental-first content. |
| ICP-004 Entrepreneur / Company Formation | Primary design set | Top-level pathway, company formation, substance, tax, VAT, accounting, and banking service routes. |
| ICP-005 HNI Permanent Residency | Primary design set | Top-level permanent residency pathway, PR by investment, property requirements, tax, due diligence, and wealth planning experts. |
| ICP-006 Family Relocating with Children | Primary design set | Top-level family pathway, schools, healthcare, areas, rentals, and longer nurture journey. |
| ICP-001 UK National Retiree | Primary design set | Top-level retiree pathway, Category F, pensions, healthcare, post-Brexit residency, and property journey. |
| ICP-003 Non-EU Digital Nomad | Secondary acquisition audience | Content cluster only; not dominant in main navigation. |
| ICP-007 Property Speculators | Strategic content audience | Property due diligence, investor comparison, area pages, and developer-neutral trust surfaces. |
| ICP-009 Low Budget Escapers | Nurture/filter case | Single lightweight route page, FAQ and checklist content, not premium partner flow. |
| ICP-008 Related Partners | Internal stakeholder | Expert hub and referral disclosure support partner trust without public partner names. |

---

## Pages Consolidated or Renamed in This Rebuild

These 10 page concepts from the previous inventory do not have a matching URL slug in the new sitemap. None had a process-doc link in the old version, so no process-doc references are broken, but flag if any of this content was in progress:

| Old slug | Likely new equivalent |
|---|---|
| /entrepreneurs/cyprus-corporate-tax | Not present in new sitemap — was P1 idea only |
| /entrepreneurs/ip-box-regime | Not present in new sitemap — was P1 idea only |
| /entrepreneurs/personal-vs-company-residency | Not present in new sitemap — was P1 idea only |
| /families/mixed-nationality-families | Not present in new sitemap — was P1 idea only |
| /permanent-residency/maintaining-pr | Not present in new sitemap — was P1 idea only |
| /property-investors/rental-yields-paphos | Not present in new sitemap — was P2 idea only |
| /property-investors/repossessed-properties | Not present in new sitemap — was P2 idea only |
| /settling-in/cost-of-living-paphos | /tools/paphos-cost-calculator (P131) + /resources/blog/paphos-cost-of-living-update (P153) |
| /tools/company-formation-checklist | Not present in new sitemap — was P1 idea only |
| /tools/first-30-days-checklist | /tools/move-timeline (P135) |

---

## 1. Core / Utility

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P001 | / | Moving to Cyprus from the UK, with a Clear Route | Home | P0 | MOFU | moving to Cyprus from UK | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P002 | /about | About Paphos Advisor | About | P0 | MOFU | Paphos Advisor | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P003 | /about/editorial-policy | Our Editorial Policy | About | P1 | MOFU | Paphos Advisor editorial policy | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P004 | /about/referral-disclosure | Referral Disclosure | About | P0 | BOFU | Cyprus referral disclosure | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P005 | /contact | Contact Paphos Advisor | Contact | P0 | BOFU | contact Paphos Advisor | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P006 | /start | Start Your Cyprus Relocation Plan | Lead Magnet | P0 | BOFU | Cyprus relocation plan | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P007 | /legal/privacy-policy | Privacy Policy | Legal | P0 | BOFU | Paphos Advisor privacy policy | — | — | idea |
| P008 | /legal/terms | Terms of Use | Legal | P0 | BOFU | Paphos Advisor terms of use | — | — | idea |
| P009 | /legal/cookie-policy | Cookie Policy | Legal | P0 | BOFU | Paphos Advisor cookie policy | — | — | idea |
| P010 | /legal | Legal Information | Legal | P1 | BOFU | Paphos Advisor legal information | — | — | idea |

---

## 2. ICP Pathway Hubs

### 2a. Remote Workers

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P011 | /remote-workers | Remote Workers Moving to Paphos | Pillar/Hub | P0 | MOFU | remote workers Paphos | ICP-002 | — | idea |

### 2b. Entrepreneurs

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P012 | /entrepreneurs | Entrepreneurs Moving to Cyprus | Pillar/Hub | P0 | MOFU | entrepreneurs moving to Cyprus | ICP-004 | — | idea |
| P030 | /entrepreneurs/company-formation-cyprus | Cyprus Company Formation Guide | FAQ | P0 | MOFU | Cyprus company formation | ICP-004 | [company-formation.md](../../../processes/business/company-formation.md) | idea |
| P031 | /entrepreneurs/running-foreign-business-from-cyprus | Running a Foreign Business from Cyprus | FAQ | P1 | MOFU | running foreign business from Cyprus | ICP-004 | — | idea |
| P032 | /entrepreneurs/cyprus-company-substance | Cyprus Company Substance Guide | FAQ | P1 | MOFU | Cyprus company substance | ICP-004 | — | idea |

### 2c. Permanent Residency

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P013 | /permanent-residency | Cyprus Permanent Residency Path | Pillar/Hub | P0 | MOFU | Cyprus permanent residency | ICP-005 | — | idea |
| P033 | /permanent-residency/investment-route | Cyprus Permanent Residency by Investment | FAQ | P0 | MOFU | Cyprus PR by investment | ICP-005 | [permanent-residency-investment.md](../../../processes/immigration/permanent-residency-investment.md) | idea |
| P034 | /permanent-residency/property-requirements | Cyprus PR Property Requirements | FAQ | P1 | MOFU | Cyprus PR property requirements | ICP-005 | [permanent-residency-investment.md](../../../processes/immigration/permanent-residency-investment.md) | idea |

### 2d. Families

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P014 | /families | Families Moving to Paphos | Pillar/Hub | P0 | MOFU | families moving to Paphos | ICP-006 | — | idea |
| P035 | /families/schools-in-paphos | Schools in Paphos Guide | FAQ | P0 | TOFU | schools in Paphos | ICP-006 | — | idea |
| P036 | /families/international-schools | International Schools in Paphos | FAQ | P1 | TOFU | international schools Paphos | ICP-006 | — | idea |
| P037 | /families/healthcare-for-children | Healthcare for Families in Paphos | FAQ | P1 | TOFU | healthcare for families Paphos | ICP-006 | [accessing-gesy-services.md](../../../processes/healthcare/accessing-gesy-services.md) | idea |

### 2e. Retirees

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P015 | /retirees | Retiring in Paphos, Cyprus | Pillar/Hub | P0 | MOFU | retiring in Paphos | ICP-001 | — | idea |
| P038 | /retirees/category-f-residency | Category F Cyprus Residency Guide | FAQ | P0 | MOFU | Category F Cyprus | ICP-001 | [category-f-permanent-residency.md](../../../processes/immigration/category-f-permanent-residency.md) | idea |
| P039 | /retirees/uk-pensions-cyprus | UK Pensions in Cyprus Guide | FAQ | P1 | MOFU | UK pensions Cyprus | ICP-001 | — | idea |

### 2f. Digital Nomads (P2)

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P016 | /digital-nomads | The Cyprus Digital Nomad Visa | Pillar/Hub | P1 | MOFU | Cyprus digital nomad visa | ICP-003 | [digital-nomad-visa.md](../../../processes/immigration/digital-nomad-visa.md) | idea |

### 2g. Property Investors (P2)

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P017 | /property-investors | Paphos Property Investors | Pillar/Hub | P2 | MOFU | Paphos property investors | ICP-007 | — | idea |

### 2h. Budget Movers (P2)

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P018 | /budget-movers | Moving to Cyprus on a Budget | Pillar/Hub | P2 | MOFU | moving to Cyprus on a budget | ICP-009 | — | idea |

---

## 3. Cross-ICP Topic Hubs

### 3a. Tax & Residency

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P019 | /tax-residency | Cyprus Tax and Residency Hub | Pillar/Hub | P0 | MOFU | Cyprus tax residency | ICP-001, ICP-002, ICP-004, ICP-005 | — | idea |
| P023 | /tax-residency/yellow-slip | Yellow Slip Cyprus Guide | FAQ | P0 | TOFU | yellow slip Cyprus | ICP-002 | [yellow-slip-eu-national.md](../../../processes/immigration/yellow-slip-eu-national.md) | idea |
| P024 | /tax-residency/yellow-slip-documents | Yellow Slip Documents Checklist | FAQ | P1 | TOFU | yellow slip documents Cyprus | ICP-002 | [yellow-slip-eu-national.md](../../../processes/immigration/yellow-slip-eu-national.md) | idea |
| P025 | /tax-residency/60-day-rule | Cyprus 60-Day Rule Guide | FAQ | P0 | MOFU | Cyprus 60-day rule | ICP-002, ICP-004, ICP-005 | [60-day-rule.md](../../../processes/tax/60-day-rule.md) | idea |
| P026 | /tax-residency/183-day-rule | Cyprus 183-Day Rule Guide | FAQ | P1 | TOFU | Cyprus 183-day rule | ICP-001, ICP-005, ICP-006 | [60-day-rule.md](../../../processes/tax/60-day-rule.md) | idea |
| P027 | /tax-residency/non-dom | Cyprus Non-Dom Guide | FAQ | P0 | MOFU | Cyprus non-dom | ICP-002, ICP-004, ICP-005 | [non-dom-status.md](../../../processes/tax/non-dom-status.md) | idea |
| P028 | /tax-residency/gesy-contributions | GESY Contributions Explained | Pillar/Hub | P1 | TOFU | GESY contributions Cyprus | ICP-001, ICP-002, ICP-004, ICP-006 | [accessing-gesy-services.md](../../../processes/healthcare/accessing-gesy-services.md) | idea |
| P029 | /tax-residency/uk-to-cyprus-tax | UK to Cyprus Tax Planning | Pillar/Hub | P1 | MOFU | UK to Cyprus tax planning | ICP-001, ICP-004, ICP-005 | — | idea |

### 3b. Property

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P020 | /property | Paphos Property Hub | Pillar/Hub | P0 | MOFU | Paphos property | ICP-001, ICP-005, ICP-006, ICP-007 | — | idea |
| P044 | /property/buying-property-paphos | Buying Property in Paphos | Pillar/Hub | P0 | MOFU | buying property in Paphos | ICP-001, ICP-005, ICP-006, ICP-007 | [buying-a-property.md](../../../processes/property/buying-a-property.md) | idea |
| P045 | /property/buyer-due-diligence | Paphos Property Due Diligence | Pillar/Hub | P1 | MOFU | Paphos property due diligence | ICP-005, ICP-007 | — | idea |
| P046 | /property/renting-in-paphos | Renting in Paphos Guide | FAQ | P1 | TOFU | renting in Paphos | ICP-001, ICP-002, ICP-006 | [renting-a-property.md](../../../processes/property/renting-a-property.md) | idea |

### 3c. Settling In

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P021 | /settling-in | Settling In Paphos Hub | Pillar/Hub | P1 | TOFU | settling in Paphos | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P040 | /settling-in/bank-account | Opening a Cyprus Bank Account | Pillar/Hub | P0 | TOFU | open Cyprus bank account | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | [bank-account-opening.md](../../../processes/settling-in/bank-account-opening.md) | idea |
| P041 | /settling-in/gesy | GESY Healthcare Guide | FAQ | P0 | TOFU | GESY Cyprus | ICP-001, ICP-002, ICP-006 | [gesy-registration.md](../../../processes/settling-in/gesy-registration.md) | idea |
| P042 | /settling-in/utilities | Setting Up Utilities in Paphos | Pillar/Hub | P1 | TOFU | set up utilities Paphos | ICP-001, ICP-002, ICP-006 | — | idea |
| P043 | /settling-in/driving-in-cyprus | Driving in Cyprus Guide | FAQ | P1 | TOFU | driving in Cyprus | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | [driving-licence-exchange.md](../../../processes/settling-in/driving-licence-exchange.md) | idea |

### 3d. Resources

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P022 | /resources | Cyprus Relocation Resources | Pillar/Hub | P0 | TOFU | Cyprus relocation resources | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |

---

## 4. Services

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P047 | /services | Cyprus Relocation Services | Service | P0 | BOFU | Cyprus relocation services | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P048 | /services/legal | Cyprus Legal Services for Relocation | Service | P0 | BOFU | Cyprus legal services | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P049 | /services/tax | Cyprus Tax Advisory Referrals | Service | P0 | BOFU | Cyprus tax advisor | ICP-001, ICP-002, ICP-004, ICP-005 | — | idea |
| P050 | /services/company-formation | Cyprus Company Formation Services | Service | P0 | BOFU | Cyprus company formation services | ICP-004 | — | idea |
| P051 | /services/property | Paphos Property Services | Service | P0 | BOFU | Paphos property services | ICP-001, ICP-005, ICP-006, ICP-007 | — | idea |
| P052 | /services/education | Paphos Education Support | Service | P1 | BOFU | Paphos education support | ICP-006 | — | idea |
| P053 | /services/healthcare | Cyprus Healthcare Navigation | Service | P1 | BOFU | Cyprus healthcare navigation | ICP-001, ICP-005, ICP-006 | — | idea |
| P054 | /services/settling-in | Paphos Settling-In Support | Service | P1 | BOFU | Paphos settling in support | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P055 | /services/banking | Cyprus Banking Introductions | Service | P1 | BOFU | Cyprus banking introductions | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P056 | /services/transport | Cyprus Transport Services | Service | P1 | BOFU | Cyprus transport services | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P057 | /services/legal/yellow-slip | Yellow Slip Legal Support | Sub-service | P0 | BOFU | yellow slip legal support | ICP-002 | [yellow-slip-eu-national.md](../../../processes/immigration/yellow-slip-eu-national.md) | idea |
| P058 | /services/legal/permanent-residency | Permanent Residency Legal Support | Sub-service | P0 | BOFU | permanent residency lawyer Cyprus | ICP-005 | [permanent-residency-investment.md](../../../processes/immigration/permanent-residency-investment.md) | idea |
| P059 | /services/legal/category-f | Category F Legal Support | Sub-service | P1 | BOFU | Category F legal support | ICP-001 | [category-f-permanent-residency.md](../../../processes/immigration/category-f-permanent-residency.md) | idea |
| P060 | /services/legal/property-conveyancing | Cyprus Property Conveyancing | Sub-service | P0 | BOFU | Cyprus property conveyancing | ICP-001, ICP-005, ICP-006 | — | idea |
| P061 | /services/tax/non-dom-planning | Cyprus Non-Dom Tax Planning | Sub-service | P0 | BOFU | Cyprus non-dom tax planning | ICP-002, ICP-004, ICP-005 | [non-dom-status.md](../../../processes/tax/non-dom-status.md) | idea |
| P062 | /services/tax/60-day-rule | Cyprus 60-Day Rule Tax Advice | Sub-service | P0 | BOFU | Cyprus 60-day rule tax advice | ICP-002, ICP-004 | [60-day-rule.md](../../../processes/tax/60-day-rule.md) | idea |
| P063 | /services/tax/uk-to-cyprus | UK to Cyprus Tax Advice | Sub-service | P1 | BOFU | UK to Cyprus tax advice | ICP-001, ICP-004, ICP-005 | — | idea |
| P064 | /services/tax/uk-pensions | UK Pension Tax Advice Cyprus | Sub-service | P1 | BOFU | UK pension tax advice Cyprus | ICP-001 | — | idea |
| P065 | /services/company-formation/cyprus-limited-company | Cyprus Limited Company Setup | Sub-service | P0 | BOFU | Cyprus limited company setup | ICP-004 | [company-formation.md](../../../processes/business/company-formation.md) | idea |
| P066 | /services/company-formation/bank-account | Cyprus Company Bank Account Help | Sub-service | P1 | BOFU | Cyprus company bank account | ICP-004 | — | idea |
| P067 | /services/company-formation/accounting | Cyprus Accounting Referrals | Sub-service | P1 | BOFU | Cyprus accounting referrals | ICP-004 | — | idea |
| P068 | /services/property/conveyancing | Paphos Property Lawyer Referral | Sub-service | P0 | BOFU | Paphos property lawyer | ICP-001, ICP-005, ICP-006 | — | idea |
| P069 | /services/property/buyer-due-diligence | Property Buyer Due Diligence | Sub-service | P0 | BOFU | property buyer due diligence Cyprus | ICP-005, ICP-007 | — | idea |
| P070 | /services/property/search | Paphos Property Search Support | Sub-service | P1 | BOFU | Paphos property search support | ICP-001, ICP-005, ICP-006 | — | idea |
| P071 | /services/property/real-estate-agent | Paphos Real Estate Agent Referral | Sub-service | P1 | BOFU | Paphos real estate agent referral | ICP-001, ICP-005, ICP-006 | — | idea |
| P072 | /services/education/school-admissions | Paphos School Admissions Support | Sub-service | P1 | BOFU | Paphos school admissions support | ICP-006 | — | idea |
| P073 | /services/healthcare/health-insurance | Cyprus Health Insurance Referral | Sub-service | P1 | BOFU | Cyprus health insurance referral | ICP-001, ICP-005, ICP-006 | [private-health-insurance.md](../../../processes/healthcare/private-health-insurance.md) | idea |
| P074 | /services/settling-in/utilities | Paphos Utility Setup Support | Sub-service | P2 | BOFU | Paphos utility setup support | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P075 | /services/banking/bank-introductions | Cyprus Bank Introductions | Sub-service | P1 | BOFU | Cyprus bank introductions | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | [bank-account-opening.md](../../../processes/settling-in/bank-account-opening.md) | idea |
| P076 | /services/transport/car-import | Cyprus Car Import Support | Sub-service | P2 | BOFU | Cyprus car import support | ICP-001, ICP-006 | [vehicle-import.md](../../../processes/transport/vehicle-import.md) | idea |

---

## 5. Experts

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P077 | /experts | Cyprus Relocation Experts | Expert/Person | P0 | BOFU | Cyprus relocation experts | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P078 | /experts/immigration-lawyers | Cyprus Immigration Lawyers | Expert/Person | P1 | BOFU | Cyprus immigration lawyers | ICP-001, ICP-002, ICP-003, ICP-005 | — | idea |
| P079 | /experts/tax-advisors | Cyprus Tax Advisors | Expert/Person | P1 | BOFU | Cyprus tax advisors | ICP-001, ICP-002, ICP-004, ICP-005 | — | idea |
| P080 | /experts/accountants | Cyprus Accountants | Expert/Person | P1 | BOFU | Cyprus accountants | ICP-004 | — | idea |
| P081 | /experts/company-formation-specialists | Company Formation Specialists in Cyprus | Expert/Person | P1 | BOFU | company formation specialists Cyprus | ICP-004 | — | idea |
| P082 | /experts/property-lawyers | Paphos Property Lawyers | Expert/Person | P1 | BOFU | Paphos property lawyers | ICP-001, ICP-005, ICP-006, ICP-007 | — | idea |
| P083 | /experts/real-estate-advisors | Paphos Real Estate Advisors | Expert/Person | P1 | BOFU | Paphos real estate advisors | ICP-001, ICP-005, ICP-006, ICP-007 | — | idea |
| P084 | /experts/government-liaison | Cyprus Government Liaison Support | Expert/Person | P1 | BOFU | Cyprus government liaison | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P085 | /experts/relocation-consultants | Paphos Relocation Consultants | Expert/Person | P1 | BOFU | Paphos relocation consultants | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P086 | /experts/healthcare-navigators | Cyprus Healthcare Navigators | Expert/Person | P1 | BOFU | Cyprus healthcare navigators | ICP-001, ICP-005, ICP-006 | — | idea |
| P087 | /experts/education-advisors | Paphos Education Advisors | Expert/Person | P1 | BOFU | Paphos education advisors | ICP-006 | — | idea |
| P088 | /experts/insurance-brokers | Cyprus Insurance Brokers | Expert/Person | P1 | BOFU | Cyprus insurance brokers | ICP-001, ICP-005, ICP-006 | — | idea |
| P089 | /experts/wealth-planning-advisors | Cyprus Wealth Planning Advisors | Expert/Person | P1 | BOFU | Cyprus wealth planning advisors | ICP-005 | — | idea |

---

## 6. Locations

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P090 | /locations | Where to Live in Paphos | Location | P0 | MOFU | where to live in Paphos | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P091 | /locations/paphos | Living in Paphos | Location | P1 | MOFU | living in Paphos | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P092 | /locations/pegeia | Living in Pegeia | Location | P1 | MOFU | living in Pegeia | ICP-001, ICP-006, ICP-007 | — | idea |
| P093 | /locations/peyia | Living in Peyia | Location | P2 | MOFU | living in Peyia | ICP-001, ICP-006, ICP-007 | — | idea |
| P094 | /locations/chloraka | Living in Chloraka | Location | P1 | MOFU | living in Chloraka | ICP-001, ICP-006, ICP-007 | — | idea |
| P095 | /locations/kissonerga | Living in Kissonerga | Location | P1 | MOFU | living in Kissonerga | ICP-001, ICP-006, ICP-007 | — | idea |
| P096 | /locations/tala | Living in Tala | Location | P1 | MOFU | living in Tala | ICP-001, ICP-005, ICP-006 | — | idea |
| P097 | /locations/tsada | Living in Tsada | Location | P2 | MOFU | living in Tsada | ICP-001, ICP-005, ICP-007 | — | idea |
| P098 | /locations/kato-paphos | Living in Kato Paphos | Location | P1 | MOFU | living in Kato Paphos | ICP-001, ICP-002, ICP-007 | — | idea |
| P099 | /locations/universal | Living in Universal, Paphos | Location | P1 | MOFU | living in Universal Paphos | ICP-002, ICP-006, ICP-007 | — | idea |
| P100 | /locations/konia | Living in Konia | Location | P1 | MOFU | living in Konia | ICP-005, ICP-006 | — | idea |
| P101 | /locations/coral-bay | Living in Coral Bay | Location | P1 | MOFU | living in Coral Bay | ICP-001, ICP-005, ICP-007 | — | idea |
| P102 | /locations/mesogi | Living in Mesogi | Location | P2 | MOFU | living in Mesogi | ICP-001, ICP-006 | — | idea |
| P103 | /locations/best-areas-for-families | Best Areas in Paphos for Families | Location | P1 | MOFU | best areas in Paphos for families | ICP-006 | — | idea |
| P104 | /locations/best-areas-for-retirees | Best Areas in Paphos for Retirees | Location | P1 | MOFU | best areas in Paphos for retirees | ICP-001 | — | idea |
| P105 | /locations/best-areas-for-remote-workers | Best Paphos Areas for Remote Workers | Location | P2 | MOFU | best areas in Paphos for remote workers | ICP-002 | — | idea |

---

## 7. Compare

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P106 | /compare/cyprus-vs-malta | Cyprus vs Malta for Relocation | Comparison | P1 | MOFU | Cyprus vs Malta | ICP-002, ICP-004, ICP-005 | — | idea |
| P107 | /compare/cyprus-vs-portugal | Cyprus vs Portugal for Expats | Comparison | P2 | MOFU | Cyprus vs Portugal | ICP-001, ICP-002, ICP-005 | — | idea |
| P108 | /compare/paphos-vs-limassol | Paphos vs Limassol for Expats | Comparison | P1 | MOFU | Paphos vs Limassol | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P109 | /compare/paphos-vs-larnaca | Paphos vs Larnaca for Expats | Comparison | P2 | MOFU | Paphos vs Larnaca | ICP-001, ICP-002, ICP-006 | — | idea |
| P110 | /compare/cyprus-vs-ireland-company | Cyprus vs Ireland Company Setup | Comparison | P2 | MOFU | Cyprus vs Ireland company setup | ICP-004 | — | idea |
| P111 | /compare/rent-first-vs-buy-paphos | Rent First or Buy in Paphos? | Comparison | P1 | MOFU | rent or buy in Paphos | ICP-001, ICP-005, ICP-006 | — | idea |

---

## 8. Support (Glossary, FAQ, Tools)

### 8a. Glossary

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P112 | /glossary | Cyprus Relocation Glossary | Glossary | P1 | TOFU | Cyprus relocation glossary | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P113 | /glossary/yellow-slip | What Is a Cyprus Yellow Slip? | Glossary | P1 | TOFU | what is a Yellow Slip | ICP-002 | [yellow-slip-eu-national.md](../../../processes/immigration/yellow-slip-eu-national.md) | idea |
| P114 | /glossary/meu1 | What Is MEU1 in Cyprus? | Glossary | P1 | TOFU | MEU1 Cyprus | ICP-002 | [yellow-slip-eu-national.md](../../../processes/immigration/yellow-slip-eu-national.md) | idea |
| P115 | /glossary/category-f | What Is Category F Residency? | Glossary | P1 | TOFU | Category F residency Cyprus | ICP-001 | [category-f-permanent-residency.md](../../../processes/immigration/category-f-permanent-residency.md) | idea |
| P116 | /glossary/non-dom | What Is Cyprus Non-Dom? | Glossary | P1 | TOFU | Cyprus non-dom meaning | ICP-002, ICP-004, ICP-005 | [non-dom-status.md](../../../processes/tax/non-dom-status.md) | idea |
| P117 | /glossary/60-day-rule | What Is the Cyprus 60-Day Rule? | Glossary | P1 | TOFU | Cyprus 60-day rule meaning | ICP-002, ICP-004 | [60-day-rule.md](../../../processes/tax/60-day-rule.md) | idea |
| P118 | /glossary/gesy | What Is GESY in Cyprus? | Glossary | P1 | TOFU | what is GESY | ICP-001, ICP-002, ICP-006 | [gesy-registration.md](../../../processes/settling-in/gesy-registration.md) | idea |
| P119 | /glossary/title-deeds | What Are Title Deeds in Cyprus? | Glossary | P1 | TOFU | title deeds Cyprus | ICP-005, ICP-006, ICP-007 | — | idea |
| P120 | /glossary/crmd | What Is CRMD in Cyprus? | Glossary | P1 | TOFU | CRMD Cyprus | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |

### 8b. FAQ

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P121 | /faq | Cyprus Relocation FAQ | FAQ | P0 | TOFU | Cyprus relocation FAQ | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P122 | /faq/residency | Cyprus Residency FAQ | FAQ | P1 | TOFU | Cyprus residency FAQ | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P123 | /faq/tax | Cyprus Tax Residency FAQ | FAQ | P1 | TOFU | Cyprus tax residency FAQ | ICP-001, ICP-002, ICP-004, ICP-005 | — | idea |
| P124 | /faq/property | Paphos Property FAQ | FAQ | P1 | TOFU | Paphos property FAQ | ICP-001, ICP-005, ICP-006, ICP-007 | — | idea |
| P125 | /faq/families | Moving to Paphos with Family FAQ | FAQ | P1 | TOFU | moving to Paphos with family FAQ | ICP-006 | — | idea |
| P126 | /faq/company-formation | Cyprus Company Formation FAQ | FAQ | P1 | TOFU | Cyprus company formation FAQ | ICP-004 | — | idea |

### 8c. Tools / Lead Magnets

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P127 | /tools | Cyprus Relocation Tools | Lead Magnet | P1 | MOFU | Cyprus relocation tools | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P128 | /tools/relocation-route-finder | Cyprus Relocation Route Finder | Lead Magnet | P1 | MOFU | Cyprus relocation route finder | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P129 | /tools/yellow-slip-checklist | Yellow Slip Checklist | Lead Magnet | P1 | MOFU | Yellow Slip checklist | ICP-002 | [yellow-slip-eu-national.md](../../../processes/immigration/yellow-slip-eu-national.md) | idea |
| P130 | /tools/cyprus-tax-route-finder | Cyprus Tax Route Finder | Lead Magnet | P2 | MOFU | Cyprus tax route finder | ICP-002, ICP-004, ICP-005 | — | idea |
| P131 | /tools/paphos-cost-calculator | Paphos Cost of Living Calculator | Lead Magnet | P2 | MOFU | Paphos cost of living calculator | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P132 | /tools/permanent-residency-readiness | Cyprus Permanent Residency Readiness Checklist | Lead Magnet | P1 | MOFU | Cyprus PR readiness checklist | ICP-005 | — | idea |
| P133 | /tools/family-move-checklist | Paphos Family Move Checklist | Lead Magnet | P1 | MOFU | Paphos family move checklist | ICP-006 | — | idea |
| P134 | /tools/retirement-move-checklist | Cyprus Retirement Move Checklist | Lead Magnet | P1 | MOFU | Cyprus retirement checklist | ICP-001 | — | idea |
| P135 | /tools/move-timeline | Cyprus Move Timeline Planner | Lead Magnet | P2 | MOFU | Cyprus move timeline | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |

---

## 9. Blog

Seasonality and schema notes for each post are in `sitemap-full-metadata.csv`. All 18 posts are `BlogPosting + Article + BreadcrumbList` schema.

| page-id | url-slug | h1 | type | phase | funnel-stage | primary-keyword | icp | process-doc | status |
|---------|----------|----|------|-------|-------------|----------------|-----|------------|--------|
| P136 | /resources/blog/cyprus-immigration-updates | Cyprus Immigration Updates | Blog | P1 | TOFU | Cyprus immigration updates | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P137 | /resources/blog/cyprus-tax-updates-expats | Cyprus Tax Updates for Expats | Blog | P1 | TOFU | Cyprus tax updates expats | ICP-001, ICP-002, ICP-004, ICP-005 | — | idea |
| P138 | /resources/blog/yellow-slip-mistakes | Common Yellow Slip Mistakes | Blog | P2 | TOFU | Yellow Slip mistakes | ICP-002 | — | idea |
| P139 | /resources/blog/category-f-mistakes | Category F Mistakes to Avoid | Blog | P2 | TOFU | Category F mistakes | ICP-001 | — | idea |
| P140 | /resources/blog/non-dom-myths-cyprus | Cyprus Non-Dom Myths | Blog | P2 | TOFU | Cyprus non-dom myths | ICP-002, ICP-004, ICP-005 | — | idea |
| P141 | /resources/blog/paphos-property-market-update | Paphos Property Market Update | Blog | P1 | TOFU | Paphos property market update | ICP-001, ICP-005, ICP-006, ICP-007 | — | idea |
| P142 | /resources/blog/property-scams-cyprus | Property Scams in Cyprus | Blog | P2 | TOFU | property scams Cyprus | ICP-005, ICP-007 | — | idea |
| P143 | /resources/blog/school-admissions-paphos | Paphos School Admissions Tips | Blog | P2 | TOFU | Paphos school admissions | ICP-006 | — | idea |
| P144 | /resources/blog/summer-in-paphos | Summer in Paphos | Blog | P2 | TOFU | summer in Paphos | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P145 | /resources/blog/winter-in-paphos | Winter in Paphos | Blog | P2 | TOFU | winter in Paphos | ICP-001, ICP-002 | — | idea |
| P146 | /resources/blog/best-restaurants-new-residents-paphos | Best Restaurants for New Residents in Paphos | Blog | P2 | TOFU | best restaurants Paphos new residents | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P147 | /resources/blog/events-in-paphos | Events in Paphos for New Residents | Blog | P2 | TOFU | events in Paphos | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P148 | /resources/blog/making-friends-in-paphos | Making Friends in Paphos | Blog | P2 | TOFU | making friends in Paphos | ICP-001, ICP-002, ICP-006 | — | idea |
| P149 | /resources/blog/running-uk-company-from-cyprus-risks | Running a UK Company from Cyprus Risks | Blog | P2 | TOFU | running UK company from Cyprus risks | ICP-004 | — | idea |
| P150 | /resources/blog/cyprus-vat-mistakes | Cyprus VAT Mistakes | Blog | P2 | TOFU | Cyprus VAT mistakes | ICP-004 | — | idea |
| P151 | /resources/blog/rent-before-buying-paphos | Should You Rent Before Buying in Paphos? | Blog | P2 | TOFU | rent before buying Paphos | ICP-001, ICP-005, ICP-006 | — | idea |
| P152 | /resources/blog/cyprus-bureaucracy-realities | Cyprus Bureaucracy Realities | Blog | P2 | TOFU | Cyprus bureaucracy | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
| P153 | /resources/blog/paphos-cost-of-living-update | Paphos Cost of Living Update | Blog | P2 | TOFU | Paphos cost of living update | ICP-001, ICP-002, ICP-004, ICP-005, ICP-006 | — | idea |
