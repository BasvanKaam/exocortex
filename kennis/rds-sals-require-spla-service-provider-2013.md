---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure, rds, sal, spla, licensing]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# RDS SALs required SPLA / service-provider status (2013)

How it worked then: to use RDS functionality on Azure (limited to Hosted Shared Desktops) you needed the newly introduced RDS Subscriber Access Licenses (SALs). RDS SALs were offered only as part of Microsoft's Services Provider Licensing Agreement (SPLA), so you had to be a Microsoft Services Provider to obtain them.

Crucially, RDS Client Access Licenses (CALs) bought through Volume Licensing such as Enterprise Agreements did NOT get License Mobility to shared cloud platforms, so plain CALs could not be used on Azure. A workaround was to obtain SPLA licensing yourself, which made your company a service provider in Microsoft's eyes. The practical effect: not every enterprise could just move RDS onto Azure.

*Bron: blogpost 'Why you shouldn't deploy XD7 on Azure just yet.' (2013-08-18), basvankaam.com.*

## Verwante notities

- [Client OSes were not allowed on multi-tenant public cloud (2013 licensing)](client-os-not-allowed-multitenant-cloud-2013.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Positie: the Citrix XD7-on-Azure design guide was misleading marketing](positie-citrix-azure-design-guide-confusing-2013.md)
