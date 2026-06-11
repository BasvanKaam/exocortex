---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [daas, licensing, microsoft, workspaces, hosted-shared]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Why DaaS rarely gives you a real client OS (licensing)

How it worked then (2013): the reason most DaaS offers were not real Windows 7/8 client desktops came down to Microsoft licensing. Per the Product Use Rights, multi-tenant hosting of Windows client desktops (Windows 7, Windows 8) was restricted, so client OS desktops were not available on Azure, Amazon or other service providers.

Consequence: about 75% of DaaS used the Hosted Shared Desktop (HSD / RDS) model on a server OS. Amazon WorkSpaces was the exception in that it ran single-user Windows Server 2008 R2 one-on-one (one user per server desktop) with a Windows 7 user experience and persistent storage, but it was still a server OS, not a client OS.

*Bron: blogpost 'DaaS has grown up... Has it?' (2013-11-14), basvankaam.com.*

## Verwante notities

- [Amazon WorkSpaces architecture (2013 preview)](amazon-workspaces-2013-architecture.md)
- [Client OSes were not allowed on multi-tenant public cloud (2013 licensing)](client-os-not-allowed-multitenant-cloud-2013.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Don't be fooled: DaaS marketing sells a client desktop you aren't actually getting](daas-marketing-vs-reality.md)
- [Microsoft SPLA and why true DaaS is restricted](microsoft-spla-daas-licensing-restriction.md)
- [Delivering a desktop OS multi-tenant via dedicated Moonshot cartridges](moonshot-desktop-os-multi-tenancy-licensing.md)
- [Positie: the cloud blocker is Microsoft licensing, not the product](positie-blame-microsoft-licensing-not-citrix.md)
- [Positie: the Citrix XD7-on-Azure design guide was misleading marketing](positie-citrix-azure-design-guide-confusing-2013.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
- [Server VDI is an underrated, overlooked feature](server-vdi-underrated.md)
- [Server VDI vs Hosted Shared Desktop in XenDesktop 7](server-vdi-vs-hsd.md)
- [Why true Windows desktop DaaS was blocked by SPLA](splash-spla-no-true-windows-daas.md)
- [VDI vs RDS vs DaaS, the core distinction](vdi-rds-daas-distinction.md)
- [VDI and DaaS are distinct, not interchangeable](vdi-versus-daas-distinct-solutions.md)
- [WVD introduced multi-user Windows 10 and a license-based entitlement model](wvd-win10-multiuser-and-licensing.md)
