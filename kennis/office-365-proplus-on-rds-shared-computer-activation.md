---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [office-365, rds, shared-computer-activation, vdi, euc]
layer: reference
gedateerd: ja
bron: salomon-whitepaper
---

# ProPlus on RDS and shared computer activation

ProPlus is allowed on Remote Desktop Services (multiple users on one server OS, often combined with Citrix or VMware). It requires the Office Deployment Tool configured for shared computer activation, which bypasses the normal per-device install limits where many users log in with their own account. Each user who can use the software still needs a license. Shared computer activation is not available for Mac users.

Dated constraint (circa 2019): ProPlus was supported on Windows 10 and Windows Server 2016 but NOT Windows Server 2019. So for RDS plus ProPlus you stayed on Server 2016, or chose perpetual Office 2019 with Server 2019. Building a base image with ProPlus has its own pitfalls.

*Bron: Salomon-IT 'Whitepaper - Ofifce 365 ProPlus implementeren en onderhouden - gecorrigeerd - Copy'.*

## Verwante notities

- [From Terminal Services to AVD - The Multi-User History](history-terminal-services-to-avd.md)
- [Office 365 ProPlus on Remote Desktop Services](o365-proplus-on-rds.md)
- [ProPlus pre-rollout inventory checklist](office-365-proplus-inventory-before-rollout.md)
- [Prefer ProPlus for its licensing model and flexibility](office-vs-proplus-license-and-flexibility-stance.md)
- [Citrix says supported, Microsoft says not: reading two support matrices at once](vendor-support-matrix-contradictions.md)
- [Windows 10 Multi-User (Azure-only) and ProPlus](windows-10-multi-user-azure-only.md)
