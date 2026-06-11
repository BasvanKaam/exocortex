---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [scaf, cloud-migration, inventory, assessment, cloud-masterclass, template]
layer: reference
gedateerd: nee
bron: salomon-masterclass
---

# SCAF Wave 3 application inventory palette

The per-application worksheet Bas uses in Wave 3 of the SCAF (Step-Cloud Adoptie Framework) to inventory application, data and system before deciding how to migrate. One palette is completed per application/system, then the inputs drive a migration strategy and rationale. Structure of the palette:

- Identification: application/system name, department, version, date.
- Licenses: license type, number in use, number available.
- Organizational impact: strategic weight (high/medium/low), teams involved (e.g. HR, Finance), estimated lead time (days/weeks/months).
- Drivers: the (up to three) reasons this app should go to cloud.
- Financial impact: current situation vs. coming situation, with notes.
- Operational impact (per dependency): agreed SLAs (e.g. 24x7, 99.8% uptime), maintenance windows, management load in hours/week.
- Dependencies: application type (container, installed, virtualized), footprint (CPU, memory, storage, network), databases, middleware, other.
- Application risk profile: availability, data corruption/leak, vendor bankruptcy or acquisition, excessive cost; each leading to a follow-up choice: control, accept, or eliminate.
- Migration strategy / cloud technology: Retain / Refactor / Rehost / Repurchase / Retire, mapped to a target model (IaaS, PaaS, DaaS, SaaS).
- Conclusion / rationale.

Method insight: the palette forces risk and dependency analysis BEFORE the migration verb (the R) is chosen, so the strategy falls out of the evidence rather than being assumed up front.

*Bron: Salomon-IT 'SCAF - Wave 3 - Applicatie, data en systeem inventarisatie palet - Copy'.*

## Verwante notities

- [Criteria for Selecting the First Workload to Migrate](first-workload-selection-criteria.md)
