---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [opdracht, 6-rs, governance, exercise, azure-migrate, healthcare]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Opdracht 7: Cloud Migration Compass (XYZ-Care Health Group)

Bas's exercise "Cloudmigratie Kompas: Inventariseren En Sturen" uses a fictional organization, **XYZ-Care Health Group**, which runs a mix of legacy systems and modern tools. The task: make a first inventory and tackle governance challenges.

**Assignment**: map current applications and categorize them per the 6 R's (here phrased as Rehost, Refactor, Rearchitect, Rebuild, Replace, Retire), with justification (it's a first inventory round; definitive choices come later). Identify governance challenges/bottlenecks specific to XYZ-Care's migration and draft guidelines. An extended business case is optional at this point.

**Worked example** (using an inventory tool such as Azure Migrate):
- **Rehost**: the planning tool (a SaaS solution) moves unchanged to a new Cloud environment.
- **Refactor**: the financial management system (outdated interfaces) needs small adjustments for better integration.
- **Rearchitect**: the Electronic Patient Record (EPD) must be adapted to function in the Cloud, modernizing its couplings with other systems.
- **Rebuild**: the reporting tool (limited scalability) must be rebuilt with modern data-analytics platforms.
- **Replace**: the outdated HRM system with limited integration is replaced by a modern Cloud-based HR platform.
- **Retire**: old unused tools/software (e.g. outdated communication apps) are phased out.

Extra attention goes to **dependencies** (e.g. integration between the EPD, planning tool and reporting tool); even if exact consequences aren't clear yet, they're written out explicitly for later analysis.

**Governance challenges identified**: data security and AVG (GDPR) compliance for sensitive patient data (guidelines for encryption, access control, monitoring); **vendor lock-in** (advice: use open standards and export options so data/apps can migrate if needed); and cost management (guidelines/policy rules to monitor and optimize Cloud usage and costs). Finally the team builds a plan to improve governance: clear roles and responsibilities, monitoring/control processes, and continuous evaluation.

## Verwante notities

- [Azure data migration and import tools](azure-data-migration-import-tools.md)
- [Bas: The 6 R's for Application Rationalization](bas-6-rs-cloud-migration.md)
- [Bas: 'Wegwerp IT' and the Lift-and-Shift Caution](bas-wegwerp-it-and-lift-and-shift.md)
- [Fictional case: XYZ-Care Health Group](case-xyz-care-health-group.md)
- [Opdracht 9: Migration Mastery - Strategy to Execution (XYZ-Care)](migration-mastery-assignment-xyz-care.md)
- [Opdracht 8: AVG in healthcare (XYZ-Care)](opdracht-8-avg-in-healthcare-xyz-care.md)
- [SCAF: Application, Data and System Inventory via Waves](scaf-application-data-system-inventory.md)
