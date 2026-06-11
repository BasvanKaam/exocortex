---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [sdn, networking, hyper-v, multi-tenant, windows-server-2012-r2]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# SDN via Hyper-V network virtualization (how it worked in 2012 R2)

How it worked then: software-defined networking in Server 2012 R2 was built from two pieces, Hyper-V network virtualization and the Hyper-V extensible switch. Together they let you run multiple virtual networks (with their own subnets, routing topologies and tenant-chosen IP ranges) over the same physical network, using overlapping IP ranges without separate VLANs. Three virtual networks all on 192.168.168.x would just work, each behaving like the only network on the shared physical fabric.

It also let admins shape and prioritise (QoS) or block traffic from a central console without reconfiguring physical switches or routers. The multi-tenant gateway (built into R2) gave site-to-site VPN connectivity for multiple customers from one interface, replacing the per-tenant gateway model. Mainly built for large hosted multi-tenant clouds, but Bas flags it as imperative to understand the concept early.

*Bron: blogpost 'A closer look at the Cloud, based on Server 2012 R2' (2013-10-26), basvankaam.com.*

## Verwante notities

- [Learn the virtual-network concept now, even if you won't deploy it soon](learn-sdn-concept-now-position.md)
- [Server 2012 R2 opened up cheaper VDI storage options](server-2012-r2-cheaper-vdi-storage.md)
- [Server 2012 R2 data dedup and the VDI separation rule](server-2012-r2-dedup-for-vdi.md)
- [Work Folders: on-premises file sync as a Dropbox alternative](work-folders-2012r2.md)
- [Workplace Join: registering devices without full domain join](workplace-join-2012r2.md)
