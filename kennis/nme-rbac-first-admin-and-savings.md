---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, rbac, log-analytics, cost-optimization, avd]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# NME first-admin RBAC and log analytics retention savings

Two durable NME operational points from Bas's review:

- First-admin RBAC: the person who installs Nerdio holds the AVD admin role by default and is initially the only one able to log into NME and hand out roles to others. Assigning roles is therefore an important first step right after installation.
- Log Analytics workspace cost: adjusting the data-retention presets on the Log Analytics workspace produces real cost savings, a powerful feature worth demonstrating.
- User cost attribution is enabled during NME installation in current versions.
- Reserved Instances are no longer part of the Modeler.
- Naming: Azure Stack HCI is now Azure Local; content should be updated accordingly.

Dated: tied to current NME versions and Azure/Microsoft naming; verify before reuse.

*Bron: Nerdio-content 'Feedback on NME-201 exam' (Training).*

## Verwante notities

- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [Nerdio non-technical cost levers](nerdio-non-technical-cost-levers.md)
- [Settings for Success: Nerdio cost-optimization checklist](nerdio-settings-for-success-cost-checklist.md)
- [How Bas reviews Nerdio L&D content as SME](nme-course-content-review-method.md)
- [NME persists machine names across reimage/rebuild](nme-hostpool-naming-persistence.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [Why Windows 365 enablement needs Global Admin (org consent)](windows-365-enablement-permissions.md)
