---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [scaf, inventory, waves, rationalization, dependencies, storage]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# SCAF: Application, Data and System Inventory via Waves

Waves 1 and 2 create an overview of all present and in-use applications, datasets, systems, (physical) network and security components, looking at the function they fulfill, their impact in/on the organization, and technical dependencies. From this you get a first picture of whether (and how) a workload can move to the Cloud, by what method (rationalization), and whether a modernization pass in wave 3 is worth the extra time.

For larger, complex IaaS-focused environments, Bas suggests limiting choices initially to **rehost and retire** (part of the 6 R's) to quickly create a starting point, then applying a more detailed analysis later.

The same process runs for data, networks, hardware components, virtual systems and storage. Document everything carefully, including required (24/7) availability, contractual restrictions and special cases. For networks watch line type, up/download speed, bandwidth and redundancy needs; for storage, the type, throughput, etc. Specific dependencies to capture include: latency sensitivity; other network requirements; where data resides in the new Cloud situation; whether all data may/should go to the Cloud; data volumes; specific storage requirements (block, file, system); dependencies on hardware/dongles, OS, other applications; single vs multi-user certification; security requirements (encryption, authentication); and minimum/desired system requirements.

Also don't forget: existing monitoring/tooling, an overview of current subscriptions and licenses, unused active resources, unexplained usage/consumption, permissions and rights, and lack of budget control.

## Verwante notities

- [Application Baseline: purpose and scope](application-baseline-purpose-and-scope.md)
- [Two-phase scan method for the Application Baseline](application-baseline-two-phase-scan.md)
- [Azure data migration and import tools](azure-data-migration-import-tools.md)
- [Bas: The 6 R's for Application Rationalization](bas-6-rs-cloud-migration.md)
- [Building a Compact Cloud Business Case](compact-cloud-business-case-method.md)
- [Selecting the First Migration Workload (Simple to Complex)](first-migration-workload-selection.md)
- [Criteria for Selecting the First Workload to Migrate](first-workload-selection-criteria.md)
- [Migrate vs Modernize as a Per-Workload Decision](migrate-vs-modernize-distinction.md)
- [Opdracht 7: Cloud Migration Compass (XYZ-Care Health Group)](opdracht-7-cloud-migration-compass.md)
- [Definitive Cloud and Refactor Choice (Rationalisation)](rationalisation-refactor-choice-execution.md)
- [SCAF execution-phase templates and the migration waves](scaf-execution-phase-templates.md)
- [SCAF Insight Phase: Actions and the Waves Approach](scaf-insight-actions-and-waves.md)
- [SCAF Chapter 8: The Insight (Inzicht) Phase Foundation](scaf-insight-phase-foundation.md)
- [SCAF insight-pillar intake workshop questions](scaf-insight-pillar-intake-questions.md)
- [SCAF Insight Phase: Results and Supporting Documentation](scaf-insight-results-and-documentation.md)
- [SCAF Insight Phase: Security Topics to Surface](scaf-security-insight-phase.md)
- [SCAF Insight: Workshop as Starting Point](scaf-workshop-starting-point.md)
- [Smart inventory for workplace and application lifecycle](smart-inventory-lifecycle-management.md)
