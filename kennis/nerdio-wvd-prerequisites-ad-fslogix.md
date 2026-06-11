---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-10
tags: [wvd, fslogix, active-directory, azure-ad-ds, networking]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles

Bas notes that Nerdio doesn't remove WVD's underlying prerequisites. As of 2020 you still need a 'classic' Active Directory (on-prem or in Azure) synced to Azure AD via Azure AD Connect, or an Azure AD DS managed domain, to run WVD. User profiles still go through FSLogix containers (VHDs) stored on a file server share; at the time, Azure Files support inside Nerdio was 'being worked on' and Azure NetApp Files was already an option.

Networking basics he calls out: your Azure VMs need a subnet that can talk to the AD DS / DC subnet; Microsoft advised same vNet, different subnet from the managed domain; point your vNet DNS at the AD DS service or DC.

Dated to 2020 WVD, but the dependency chain (directory + profile container + networking line-of-sight) is the durable shape of a session-host deployment.

*Bron: blogpost 'How to: Nerdio Manager for WVD, first steps (install + first tenant)' (2020-04-14), basvankaam.com.*

## Verwante notities

- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [Azure building blocks to extend, protect and migrate RDS/WVD](azure-services-for-rds-wvd-extend-migrate.md)
- [Nerdio Manager for WVD deploys into your own Azure tenant](nerdio-manager-wvd-deploys-in-your-tenant.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
- [Inspecting prerequisites up front saves the whole deployment](prerequisites-discipline-saves-time.md)
- [Even with managed WVD, the customer still owns the base image](wvd-customer-still-owns-the-base-image.md)
- [WVD is not a click-and-go product](wvd-not-click-and-go.md)
- [WVD preview constraints (2019)](wvd-preview-good-to-knows.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
- [WVD tenant setup gotchas (2019 workshop)](wvd-tenant-setup-gotchas-2019.md)
