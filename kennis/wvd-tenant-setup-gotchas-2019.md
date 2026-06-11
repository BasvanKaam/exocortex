---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, setup, active-directory, powershell]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD tenant setup gotchas (2019 workshop)

How it worked then, from a Microsoft NL Solution Design Workshop:

- A common first-timer mistake: skipping the 'give consent' steps to the server and client app. Client-app consent is only needed for RemoteApps in the start menu, not to build/try WVD.
- The account provisioning WVD hosts needs at least RDS-Owner permissions (assigned via PowerShell).
- Users must exist in Active Directory Domain Services (normal AD) and be synced (Azure AD Connect) to Azure AD. A user created only in Azure AD cannot log in, the account can't be added to the Remote Desktop User Group because it's not in the same domain as the machine.
- Hosts can live in any Azure region, but the WVD control plane (the management plane, formerly RDMI) was only in East US 2 during preview.
- Microsoft's machine-sizing templates were considered conservative (too low on RAM/CPU) by workshop attendees.
- The marketplace held three pre-configured WVD OS images (with/without Office ProPlus) plus Windows Server 2016; none optimized for WVD/VDI, so you fine-tuned them yourself.

*Bron: blogpost '49 facts listed - What I picked up during a WVD Solution Design Workshop' (2019-05-13), basvankaam.com.*

## Verwante notities

- [Azure building blocks to extend, protect and migrate RDS/WVD](azure-services-for-rds-wvd-extend-migrate.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [WVD App Group rules (2019)](wvd-app-groups-rules-2019.md)
- [WVD Fall vs Spring release (non-ARM vs ARM)](wvd-fall-vs-spring-release.md)
- [WVD is not a click-and-go product](wvd-not-click-and-go.md)
- [WVD preview constraints (2019)](wvd-preview-good-to-knows.md)
- [WVD roadmap signals from the 2019 workshop](wvd-roadmap-signals-2019.md)
