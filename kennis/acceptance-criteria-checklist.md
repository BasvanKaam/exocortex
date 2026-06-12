---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [acceptance-criteria, delivery, governance, checklist, salomon, consulting-tool]
layer: reference
gedateerd: nee
bron: salomon-masterclass
---

# Acceptance Criteria Checklist for System Delivery

A reusable checklist Bas uses to decide whether a delivered IT system is genuinely ready to accept into production. Each item is scored against a norm (usually yes/no, sometimes a percentage or a grade). The checklist is grouped into six categories:

- **General**: system is technically tested and passed, a user acceptance test was run, an installable product is delivered, and the required management/operations tooling is delivered.
- **Documentation**: admin training plan, infrastructure/technical design, functional design, a network overview drawing (with relations, functions, IP numbers, server names), mapped interfaces, a backup schema with backup/restore procedures, recorded permissions for the management environment, a Dutch-language admin manual with FAQ and known-error list, a User Interface Guide, sufficient in-product help, and a Dutch-language user manual with keyword index.
- **Test**: all delivery documentation available before testing starts, a production-like test environment present, all agreed tests run and passed, prior test cases handed to operations (norm >80%), a test that checks availability and performance per component, evidence the system resists intended and unintended misuse (preventing data inconsistency), all tests demonstrably executed, all findings demonstrably resolved, plus a concrete end-to-end demo test case during the acceptance meeting.
- **Management and performance**: performance meets the requirements spec (PvE), response time established, deviations from standards documented and argued, an application ping independent of application processes, release change reports, easily adjustable parameters via an interface for authorized staff (grade >=7), sufficient logging to trace faults, memory/CPU capacity figures, configuration provably meeting availability requirements, processing-time and throughput figures under varying load, disk/database/network figures aligned with operations, removal of superfluous logs, proactive problem-alerting tooling, automatic component restart after outage, maintainability without downtime, simultaneous use without significant response-time degradation, uptime/downtime registration, and an arranged maintenance/service contract.
- **Tactical management**: complete overview of delivered products, overview of infrastructure changes tied to the system, recorded couplings (nature and ownership of each), concrete SMART warranty agreements with the application vendor, described hardware, verified compatibility with existing components, and proper compartmentalization of dev/test/acceptance/production environments so each role only accesses its intended environment.
- **Security**: an authorization matrix correctly implemented, periodic password change function, logging of changes to user-ids/authorizations/passwords, logging of unauthorized access attempts, regular security updates/patches for all components (including management tooling), locked-down server rights, no readable hard-coded passwords, per-transaction logging with username and date-time stamp, documented ownership of account/password maintenance, fully designed database access rights (access, read/mutate on tables, execute on procedures, all at 100%), and uniquely identifiable users in the database.

The checklist doubles as a definition-of-done and as a governance artifact: it forces documentation, testability, operability and security to all be demonstrable before go-live, not assumed.

*Bron: Salomon-IT 'Checklist-Acceptatiecriteria-1'.*

## Verwante notities

- [Compliance and risk as operational governance](compliance-risk-operational-governance.md)
- [Scope configuration management to Acceptance and Production](config-management-scope-acceptance-production.md)
- [Detailontwerp (Detailed Design) Document Skeleton](detailontwerp-document-skeleton.md)
- [Functional Design with Functional Tests](functional-design-and-functional-tests.md)
- [SCAF Handover Checklist (Overdracht Checklist)](scaf-handover-checklist-template.md)
- [SCAF implementation/migration planning template structure](scaf-implementation-migration-template.md)
- [Technical/Functional Design as Cloud Blueprint](technical-functional-design-blueprint.md)
