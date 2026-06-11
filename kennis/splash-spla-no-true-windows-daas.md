---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [microsoft, spla, daas, licensing, cloud]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Why true Windows desktop DaaS was blocked by SPLA

How the cloud-desktop licensing reality looked in 2016. Microsoft's SPLA (Services Provider License Agreement) lets service providers license Microsoft products monthly over a three-year term to host services for customers. But for VDI it was very restrictive: there was effectively no SPLA path for multi-tenant/cloud VDI unless you used dedicated hardware per customer (tenant), all the way down through servers and storage. Even with virtualization, the physical hosts had to be dedicated per tenant. This is why true DaaS, a cloud-delivered Windows *desktop* OS, was not viable as a business case: technically possible, commercially unattractive. Result: DaaS in practice ran on XenApp/RDSH (server OS) at its base, with one-to-one server-OS-per-customer being a niche workaround. This licensing wall is exactly what later Azure Virtual Desktop / Windows 365 changes were designed to knock down, so it's useful historical context for why cloud desktops took the shape they did.

*Bron: blogpost 'Citrix licensing (and Microsoft) demystified? I need your help!' (2016-04-18), basvankaam.com.*

## Verwante notities

- [Amazon WorkSpaces architecture (2013 preview)](amazon-workspaces-2013-architecture.md)
- [Client OSes were not allowed on multi-tenant public cloud (2013 licensing)](client-os-not-allowed-multitenant-cloud-2013.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Delivering a desktop OS multi-tenant via dedicated Moonshot cartridges](moonshot-desktop-os-multi-tenancy-licensing.md)
- [Positie: the cloud blocker is Microsoft licensing, not the product](positie-blame-microsoft-licensing-not-citrix.md)
- [Positie: the Citrix XD7-on-Azure design guide was misleading marketing](positie-citrix-azure-design-guide-confusing-2013.md)
