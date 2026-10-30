# CarrierMesh — Product decision log

> Independent hypothetical product design; decisions agreed for this case study, not vendor or customer approvals.

The full PRD contains D-001 through D-036. This quick index summarizes the 15 decisions made after v0.3.

| ID | Agreed direction |
|---|---|
| D-022 | Capability-driven provider/carrier/service/account feature gating |
| D-023 | Customer-admin carrier and service restrictions; backend enforcement |
| D-024 | Explicit user override when address validation is technically unavailable; INVALID still blocked |
| D-025 | Managed connection and credential lifecycle |
| D-026 | Basic international shipping/customs; advanced duties and compliance deferred |
| D-027 | Selected optional parcel services; hazardous goods, COD and freight deferred |
| D-028 | Multi-package returns where supported, without automatic splitting |
| D-029 | Provider-reported return charges, void and refund statuses only |
| D-030 | Estimated FX comparison while preserving native rate/currency |
| D-031 | Non-purchasing lookups for unknown purchase outcomes, manual fallback |
| D-032 | Eligibility-based manifest creation and safe uncertain-outcome handling |
| D-033 | Provider-driven performance in V1; formal performance targets later |
| D-034 | Balanced adoption, operational and internal business metrics |
| D-035 | Provider certification before production activation |
| D-036 | Common ERP onboarding with provider-specific authorization |

**Important corrections:** D-026 is Option B (basic international), superseding an earlier Option C selection. D-033 is Option A for V1, Option B for a future release.

For detailed rationale, requirements and acceptance criteria, see [PRD v0.4](product-requirements.txt).