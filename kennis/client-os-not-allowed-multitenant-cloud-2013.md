---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure, licensing, rds, vdi, microsoft]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Client OSes were not allowed on multi-tenant public cloud (2013 licensing)

How it worked then (2013): Microsoft's Product Use Rights prohibited running Windows client operating systems (Windows 7/8) on multi-tenant cloud platforms such as Azure, Amazon or Rackspace. License Mobility through Software Assurance explicitly excluded the Windows client OS and desktop application products.

Consequences for Citrix on Azure at the time:
- Only Hosted Shared Desktops based on Windows Server 2008 R2 / 2012 were possible. No VDI based on client OSes.
- To deploy in Azure you needed License Mobility plus valid Software Assurance for the software.
- PVS and MCS were both unsupported in Azure; VM provisioning was manual or via Azure PowerShell.

The nuance Bas later clarified: the restriction is about MULTI-tenancy. A Citrix Service Provider offering an isolated infrastructure with dedicated underlying hardware per tenant (the 'Site isolation model') could offer client OSes from the cloud.

*Bron: blogpost 'Why you shouldn't deploy XD7 on Azure just yet.' (2013-08-18), basvankaam.com.*

## Verwante notities

- [Position: client OS VDI from the cloud needs dedicated infra, not multi-tenant Azure](blog-comments-azure-client-os-cloud-position.md)
- [Citrix Service Provider (CSP) program](citrix-service-provider-program.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Delivering a desktop OS multi-tenant via dedicated Moonshot cartridges](moonshot-desktop-os-multi-tenancy-licensing.md)
- [Positie: the cloud blocker is Microsoft licensing, not the product](positie-blame-microsoft-licensing-not-citrix.md)
- [Positie: the Citrix XD7-on-Azure design guide was misleading marketing](positie-citrix-azure-design-guide-confusing-2013.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
- [RDS SALs required SPLA / service-provider status (2013)](rds-sals-require-spla-service-provider-2013.md)
- [Why true Windows desktop DaaS was blocked by SPLA](splash-spla-no-true-windows-daas.md)
