# CarrierMesh

**Provider-neutral ERP shipping integration — an independent engineering-management portfolio case study.**

> **Project status:** Product requirements and solution design. This is a hypothetical integration, not deployed software, not affiliated with an employer or shipping vendor, and not a claim of verified provider support.

## The challenge

ERP customers may connect multiple third-party shipping aggregators. Each provider has different authentication, carrier-account identifiers, service capabilities, and transaction behavior. CarrierMesh explores a unified ERP workflow while preserving provider-specific data and financial safety.

## Product scope

- Customer-owned shipping accounts and direct customer-to-provider billing
- Provider-specific authorization behind one ERP onboarding experience
- Capability-driven carrier/service discovery and customer-admin restrictions
- Concurrent cross-provider rate shopping with normalized results
- Outbound and return labels, including supported multi-package shipments
- Safe reconciliation for uncertain label-purchase outcomes
- Eligibility-based manifests, address validation, and on-demand tracking
- Basic international customs information and selected optional parcel services
- Customer-admin access to sanitized API diagnostics
- Separate ERP-internal revenue-share audit records

## Architecture at a glance

```mermaid
flowchart LR
    U[ERP users] --> E[CarrierMesh integration]
    E --> A[Provider-neutral adapters]
    A --> P1[Shipping provider A]
    A --> P2[Shipping provider B]
    A --> P3[Shipping provider C]
    E --> C[(Tenant configuration)]
    E --> S[(Secure credentials)]
    E --> L[(Customer admin diagnostics)]
    E --> F[(Internal revenue-share ledger)]
```

## Documents

- [Product Requirements Document](docs/product/product-requirements.md)
- [Design decision log](docs/product/decision-log.md)
- [Integration architecture](docs/architecture/diagrams/01-architecture.mmd)
- [Customer onboarding](docs/architecture/diagrams/02-onboarding.mmd)
- [Rate shopping and label creation](docs/architecture/diagrams/03-rate-label.mmd)
- [Purchase recovery](docs/architecture/diagrams/04-purchase-recovery.mmd)
- [Audit/access boundaries](docs/architecture/diagrams/05-audit-access.mmd)

## Engineering trade-offs

The PRD documents **36 product design decisions**, including avoiding blind purchase retries; customer-direct billing; server-side tenant isolation; and deferring formal performance SLOs until operational baselines are measured.

## Next steps

Validate third-party provider capabilities and partner agreements, define adapter interfaces, implement a mock provider harness, and add automated acceptance tests.

**Publication disclaimer:** No production credentials, actual customer payloads, or employer-confidential material should be added to this repository.
