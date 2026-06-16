---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vda, xendesktop, limitations]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Features Server VDI cannot do

How it worked then (XenDesktop 7): Server VDI looks superior to HSD on paper (lighter install, single-user stack perks) but it drops a meaningful list of features. Not available with Server VDI:

- Personal vDisks
- HDX 3D Pro
- MS System Center
- Hosted applications (publishing apps)
- Local App Access
- Direct (non-brokered) desktop connections
- Remote PC Access

So the choice is genuinely use-case driven: if you need Generic USB redirection and don't need to publish apps, Server VDI fits; if you need any of the above, it doesn't.

*Bron: blogpost 'XenDesktop Single User Server VDI' (2014-01-06), basvankaam.com.*

## Verwante notities

- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Personal vDisk: persistence of dedicated, manageability of pooled](personal-vdisk-pvd-concept.md)
- [Server VDI is an underrated, overlooked feature](server-vdi-underrated.md)
- [Server VDI vs Hosted Shared Desktop in XenDesktop 7](server-vdi-vs-hsd.md)
- [Citrix says supported, Microsoft says not: reading two support matrices at once](vendor-support-matrix-contradictions.md)
