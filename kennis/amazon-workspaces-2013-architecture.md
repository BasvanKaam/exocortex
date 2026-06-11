---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [aws, workspaces, daas, pcoip, vpc]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Amazon WorkSpaces architecture (2013 preview)

How it worked then: provisioning WorkSpaces created a Virtual Private Cloud (VPC), connectable to on-prem AD over a secure VPN. WorkSpaces ran on EC2 instances inside the VPC; client connections used the PCoIP (PC-over-IP) protocol over TCP/UDP 4172 plus TCP 443. Persistent storage (50-100 GB depending on bundle) was backed up to S3.

Four bundles, per user per month: Standard $35, Standard Plus $50, Performance $60, Performance Plus $75. Bundles shipped Adobe Reader/Flash, Firefox, IE9, 7-Zip, JRE; Standard/Performance Plus added Office Professional and Trend Micro security. You could provision up to 5 machines at a time, ~20 minutes each. Bring-your-own-licenses supported.

*Bron: blogpost 'DaaS has grown up... Has it?' (2013-11-14), basvankaam.com.*

## Verwante notities

- [How AWS AppStream 2.0 streams apps (2019)](appstream-fleets-image-builder.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Don't be fooled: DaaS marketing sells a client desktop you aren't actually getting](daas-marketing-vs-reality.md)
- [DaaS versus VDI](daas-vs-vdi.md)
- [Don't be fooled by DaaS marketing](dont-be-fooled-by-daas-marketing-position.md)
- [On-prem is still king; a cloud 'big bang' is coming, slowly](on-prem-king-cloud-bigbang-prediction-2018.md)
- [Server VDI is an underrated, overlooked feature](server-vdi-underrated.md)
- [Why true Windows desktop DaaS was blocked by SPLA](splash-spla-no-true-windows-daas.md)
- [VDI and DaaS are distinct, not interchangeable](vdi-versus-daas-distinct-solutions.md)
