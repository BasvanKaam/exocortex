---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [functional-design, testing, acceptance-criteria, scaf]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Functional Design with Functional Tests

The functional design describes the desired functionalities and how they should work to meet user needs and business processes. By including functional tests, you ensure the described functionalities actually work, giving assurance that the finished Cloud solution meets the stated requirements.

Functional design content: description of usage goals; user requirements and functionalities (data storage, application functionality, security settings, network access); integrations between systems (on-prem and other Cloud apps, and what data they exchange); management and maintenance functions (user management, back-up procedures, monitoring); performance and scalability (response times, throughput, uptime, how it scales); security and compliance requirements (encryption, access control, data-leak protection, AVG/GDPR); and test scenarios with acceptance criteria.

Functional test scenarios each describe a specific action/function and the expected outcome, approximating reality. Bas's examples: (1) Access control test (only authorised users get in, unauthorised are blocked); (2) Data storage and retrieval test (file uploads and retrieves without corruption, validating integrity); (3) Back-up and restore test (full back-up restores without errors, checking continuity/DR); (4) Scalability test (environment auto-scales resources to absorb demand peaks without performance loss).

For each scenario a report documents test results (pass/fail and errors found), impact analysis (consequences of a failed test and affected components), and needed improvements/adjustments. After testing, run an evaluation; only when all functional tests pass and results are approved by stakeholders can the Cloud environment (or part of it) go live. Bas notes every organisation has its own templates, but structures are similar; you can Google a good template, just check you are allowed to (re)use it.

## Verwante notities

- [Acceptance Criteria Checklist for System Delivery](acceptance-criteria-checklist.md)
- [Why Write a Business Case, and Its Key Elements](business-case-value-and-elements.md)
- [DaaS / VDI Additions to the Technical Design](daas-vdi-technical-design-considerations.md)
- [SCAF Execution Phase (Uitvoeringsfase) Overview](scaf-execution-phase-overview.md)
- [SCAF GAP-analysis and Impact-analysis templates](scaf-gap-and-impact-analysis-templates.md)
- [Technical/Functional Design as Cloud Blueprint](technical-functional-design-blueprint.md)
