# Service Types Overview

## Purpose
This document summarises the service type taxonomy used across the partner system. Full definitions are in `service-type-definitions.yaml`.

The service type taxonomy defines what individual services partners provide, at a more granular level than partner category. It is used in:
- Partner records in Notion (Services Offered field)
- ICP-to-service mapping
- Referral routing logic

---

## Service Type Categories

### Immigration & Residency Services
- MEU1 (Yellow Slip) Application Handling
- MEU3 (Pink Slip) Application Handling
- Category F Permit Application
- Digital Nomad Visa Application
- Category EP (Employment Permit) Application
- Permanent Residency (Category 6.2) Application
- Naturalisation Application
- Immigration Consultation (general)
- Appeal / Rejection Handling

### Tax & Financial Services
- Cyprus Tax Residency Setup
- Non-Dom Status Application
- Personal Tax Return Filing
- Corporate Tax Planning
- Double Taxation Treaty Advice
- VAT Registration (Individual)
- VAT Registration (Company)
- Tax Consultation (general)

### Property Services
- Long-term Rental Search
- Residential Property Purchase
- Investment Property Purchase
- Conveyancing / Legal Review (property)
- Property Management

### Business Formation Services
- HE Company Formation
- Company Secretary Services
- Registered Address Services
- IP Box Regime Setup
- Payroll Services
- Social Insurance Registration

### Financial Planning Services
- UK Pension Transfer Planning (QROPS)
- Investment Portfolio Management
- Life Insurance / Protection Planning
- Wealth Structuring for Relocation
- Currency Exchange / FX

### Healthcare Services
- GP Registration (GESY)
- Medical Certificate for Permit Applications
- Private Health Insurance Guidance
- Specialist Referral

### Removal & Logistics Services
- International Household Goods Removal
- Customs Clearance (EU)
- Customs Clearance (Non-EU)
- Vehicle Transportation
- Storage Services
- Pet Transport

### Insurance Services
- Private Health Insurance
- Motor Insurance
- Property Insurance
- Life Insurance (Cyprus-based)

### Education Services
- School Selection Guidance
- Private School Application Support
- University Application Support

---

## How Service Types Are Used

When onboarding a partner, record which specific service types they offer in the Notion Partners database (Services Offered field). This enables:
- Routing the right client to the right partner
- Ensuring no gaps in our partner network
- Identifying which service areas have no coverage (and therefore need new partners)

See `partners/referral-rules/referral-routing-logic.md` for how service types map to referral decisions.
