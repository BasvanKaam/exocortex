---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vdi, rds, daas, concepts]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# VDI vs RDS vs DaaS, the core distinction

Three desktop-delivery models that are easy to conflate:

- **VDI** (Virtual Desktop Infrastructure) delivers one client-OS virtual machine per user, one-to-one, brokered to the user over a remote display protocol (RDP/ICA).
- **RDS** (Remote Desktop Services / Terminal Services) delivers a full desktop running on a single shared server OS, one desktop shared by many users at once. Also called a Hosted Shared Desktop (HSD). RDS can also publish individual applications rather than a whole desktop.
- **DaaS** (Desktop as a Service) sits in between: it is essentially VDI offered as a cloud service, where the provider takes responsibility for hosting, storage, networking, remote access, patching and backups, billed as a fixed monthly fee per machine.

The broker (RD Connection Broker, or a XenDesktop Delivery Controller) is what connects users to their assigned sessions. This taxonomy is durable even though the specific products named are dated.

*Bron: blogpost 'Desktop as a Service a.k.a. DaaS' (2013-12-13), basvankaam.com.*

## Verwante notities

- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Don't be fooled: DaaS marketing sells a client desktop you aren't actually getting](daas-marketing-vs-reality.md)
- [Server VDI is an underrated, overlooked feature](server-vdi-underrated.md)
- [Server VDI vs Hosted Shared Desktop in XenDesktop 7](server-vdi-vs-hsd.md)
- [Categorize users before choosing a desktop model](user-categorization-for-desktop-design.md)
- [VDI and DaaS are distinct, not interchangeable](vdi-versus-daas-distinct-solutions.md)
