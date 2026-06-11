---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [daas, licensing, microsoft, rds, cloud]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Why cloud DaaS ran on Server OS, not client OS (the licensing trap)

How it worked then (2013): Microsoft's Product Use Rights forbade running Windows client desktops (Windows 7/8) multi-tenant on Azure, Amazon or any other service provider. So cloud DaaS providers could not legally hand out true client-OS VDI.

The workaround: run a Windows Server OS on the back end and deliver Hosted Shared Desktops via RDS. Add the **Desktop Experience** feature so the session looks and feels like Windows 7, and most users never notice they are on a server OS.

Two escape routes from the pure-HSD limitation existed:
- **Server VDI**: a server OS delivered one-to-one per user (how Amazon WorkSpaces, on Windows Server 2008 R2, achieved true one-on-one cloud VDI). Rarely used because it is not cost-effective at scale.
- **RDS SALs** (Subscriber Access Licenses) under SPLA, enabling hosted RDS on Azure.

Reasons you might still need a real per-user (client-OS) machine: users installing their own updates/apps, modifying system-level settings, needing admin rights, heavier resource needs, or dedicated persistent storage. For those, you kept the user on-premises.

*Bron: blogpost 'Desktop as a Service a.k.a. DaaS' (2013-12-13), basvankaam.com.*

## Verwante notities

- [Amazon WorkSpaces architecture (2013 preview)](amazon-workspaces-2013-architecture.md)
- [Client OSes were not allowed on multi-tenant public cloud (2013 licensing)](client-os-not-allowed-multitenant-cloud-2013.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Don't be fooled: DaaS marketing sells a client desktop you aren't actually getting](daas-marketing-vs-reality.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
- [RDS SALs required SPLA / service-provider status (2013)](rds-sals-require-spla-service-provider-2013.md)
- [Features Server VDI cannot do](server-vdi-unsupported-features.md)
- [Server VDI vs Hosted Shared Desktop in XenDesktop 7](server-vdi-vs-hsd.md)
- [Why true Windows desktop DaaS was blocked by SPLA](splash-spla-no-true-windows-daas.md)
