---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [scaf, masterclass, migration-planning, template, workloads]
layer: reference
gedateerd: nee
bron: salomon-masterclass
---

# SCAF implementation/migration planning template structure

A concrete planning template tied to the SCAF execution phase. It describes how, when and in what manner the chosen products, services and technologies get implemented and/or migrated to the target cloud environment, making explicit who holds which responsibility, how the result is taken into operational management, and the detail planning plus expected lead time.

Template sections:
- Goal: scope of the implementation/migration plan.
- Communication: table of everyone involved with role and contact info.
- High-level description: the main steps to implement/migrate, naming which components (services, applications, systems) per step/action field, optionally referencing the technical design.
- Workloads: which products/services/components are in scope; reference to the Excel intake lists; the top 5-10 priority workloads to move first; how they move (tooling) and in what form (migration, innovation, modernization); a rationalization/refactor overview.
- Implementation requirements: resources and means needed (engineer availability, access to systems/rooms, software downloads, documentation/manuals, licenses).
- Implementation/execution schedule: each step and action in detail with a time planning (dates or week numbers) and who is involved in execution (the end-responsible is already known; multiple people or teams can execute).
- Delivery and support: what happens after a component is delivered; who decides it may go to production; who to call for support (helpdesk, are they informed?); steps to take the component into daily management, monitoring and maintenance; who must be notified and in what order. Skill readiness can play a role here.
- Expected impact / possible risk: effect on the current production environment (data preferably not in use during a move, network changes, risk of data loss/corruption, user hindrance).
- Other: free space for remarks.

This is the practical artifact a student fills in, distinct from the SCAF model itself.

*Bron: Salomon-IT 'SCAF - Cloud adoptie-migratie-implementatie planning template'.*

## Verwante notities

- [Acceptance Criteria Checklist for System Delivery](acceptance-criteria-checklist.md)
- [Criteria for Selecting the First Workload to Migrate](first-workload-selection-criteria.md)
- [Migrate vs Modernize as a Per-Workload Decision](migrate-vs-modernize-distinction.md)
- [Definitive Cloud and Refactor Choice (Rationalisation)](rationalisation-refactor-choice-execution.md)
- [SCAF Adoption-phase template as a consulting instrument](scaf-adoption-template-instrument.md)
- [SCAF Communication Plan Template](scaf-communication-plan-template.md)
- [SCAF Execution Phase (Uitvoeringsfase) Overview](scaf-execution-phase-overview.md)
- [SCAF execution-phase templates and the migration waves](scaf-execution-phase-templates.md)
