---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [scaf, cloud-masterclass, gap-analysis, skills, sourcing, template]
layer: reference
gedateerd: nee
bron: salomon-masterclass
---

# SCAF GAP-analysis worksheet: SOLL vs IST across five sourcing dispositions

A Cloud Masterclass SCAF supporting worksheet that frames the capability gap as SOLL (the desired target state) versus IST (the current state), and forces a sourcing decision per competency. Each competency is scored against five disposition columns: knowledge present in-house, train, not needed, outsource, or other.

The worksheet ships with a fixed competency list as the teaching example:
- Automation (IaC)
- Azure Backup and DR
- Role Based Access / PIM
- Azure Virtual Desktop and Cloud PC
- Load balancers and network distribution
- Identity and access management
- Cloud governance and compliance
- Application delivery
- Hypervisor layer
- Zero Trust architecture
- Network ACLs
- Basic infrastructure
- External access
- SLAs / DAPs

In the worked example, most competencies are marked as in-house knowledge present; Azure Backup/DR, load balancers, and Zero Trust are marked train; the hypervisor layer is marked not needed (cloud-native, no own hypervisor); and Azure Virtual Desktop/Cloud PC plus SLAs/DAPs are marked outsource. This models the intended teaching point: a gap analysis is not just current-vs-desired skills but an explicit per-competency sourcing decision (build, train, drop, or outsource).

The "Bij boek" variant (SCAF - GAP Analyse) is identical. Worksheet artifact specific to the training; the SCAF framework itself is already distilled from the book.

*Bron: Salomon-IT 'SCAF - GAP analyse'.*

## Verwante notities

- [A cloud GAP analysis must end in a sourcing decision, not just a skills delta](gap-analysis-is-a-sourcing-decision.md)
- [SCAF Execution Phase Supporting Documentation](scaf-execution-supporting-documentation.md)
- [SCAF GAP-analysis and Impact-analysis templates](scaf-gap-and-impact-analysis-templates.md)
- [SCAF: Knowledge, Teams, Roles and Responsibilities](scaf-knowledge-teams-raci-gap.md)
- [SCAF Toolkit: 20 downloadable templates and what's excluded](scaf-toolkit-download-and-templates.md)
