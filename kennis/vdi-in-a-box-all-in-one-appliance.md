---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, vdi-in-a-box, viab, vdi, appliance]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VDI-in-a-Box: a single all-in-one VDI appliance (how it worked)

VDI-in-a-Box (VIAB) was a single virtual appliance - the vdiManager - that bundled a connection broker, user manager, load balancer and desktop provisioning server. No shared storage required (optional), no separate management servers, no SCVMM/XenCenter/vCenter needed, running on commodity hardware with XenServer, Hyper-V or VMware. Multiple vdiManager servers could be grouped into a Grid for load balancing and high availability, using local configuration files on each host rather than a central database. Everything was managed from a single web console. The product is discontinued, but it's a clean example of the 'collapse the whole VDI stack into one appliance' design pattern.

*Bron: blogpost 'Project Curacao complete overview' (2013-05-14), basvankaam.com.*

## Verwante notities

- [VDI-in-a-Box: the simplified all-in-one VDI appliance](vdi-in-a-box-architecture.md)
- [VDI-in-a-Box served a real niche: simple, cheap, small-scale VDI](vdi-in-a-box-simple-vdi-niche.md)
- [VIAB isn't for everyone, but with the right business case it just feels right (May 2013)](viab-given-the-right-business-case-it-feels-right.md)
- [Simplicity is a feature, not a drawback (VIAB)](viab-simplicity-is-strength-position.md)
- [VIAB vs XenDesktop: simplicity vs flexibility tradeoffs (2013)](viab-vs-xendesktop-tradeoffs.md)
- [WorkspacePod is not an honest VIAB replacement (yet)](workspacepod-not-a-viab-replacement.md)
