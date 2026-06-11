---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [office-365, proplus, rds, shared-computer-activation, windows-10-multi-user, whitepaper]
layer: reference
gedateerd: ja
bron: salomon-whitepaper
---

# Office 365 ProPlus on Remote Desktop Services

From the 2019 whitepaper. ProPlus is allowed on RDS, where multiple users work on the same (usually server-OS) system configured as RDS Hosts. To run it you must use the Office Deployment Tool for 'shared computer activation', which bypasses the normal ProPlus per-device install limits for systems where multiple people log in with their own accounts. Each user still needs a separate license. Shared computer activation is NOT available for Mac users.

Key 2019 constraint Bas flags: ProPlus was supported on Windows 10 and Windows Server 2016, but NOT on Windows Server 2019. So for RDS plus ProPlus you stay on Server 2016, or pick traditional Office 2019 with Server 2019.

Windows 10 Multi-User (announced late 2018) is a desktop OS multiple users can use simultaneously (RDS for Windows 10, never seen before), available only on Azure. On it, ProPlus is fully supported by Microsoft with no end date. Building a base image with ProPlus has its own caveats.

Time-bound: these OS support boundaries are specific to 2019; Server 2019 ProPlus support and the Windows 10 Multi-User naming later evolved (Azure Virtual Desktop).

*Bron: Salomon-IT 'Whitepaper'.*

## Verwante notities

- [From Terminal Services to AVD - The Multi-User History](history-terminal-services-to-avd.md)
- [ProPlus inventory-and-choices method before rollout](o365-proplus-inventory-and-choices-method.md)
- [Office 365 ProPlus versus traditional Office](o365-proplus-vs-traditional-office.md)
- [ProPlus on RDS and shared computer activation](office-365-proplus-on-rds-shared-computer-activation.md)
- [ProPlus is usually the better choice over traditional Office](position-proplus-preferred-over-traditional-office.md)
- [Citrix says supported, Microsoft says not: reading two support matrices at once](vendor-support-matrix-contradictions.md)
- [Windows 10 Multi-User (Azure-only) and ProPlus](windows-10-multi-user-azure-only.md)
