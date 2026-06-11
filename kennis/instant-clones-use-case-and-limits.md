---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vmware, instant-clones, vdi, non-persistent, rdsh, limitations]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Instant Clones are for non-persistent floating VDI only

The primary (and at the time only sensible) use case for Instant Clones is non-persistent VDI. The constraints that force this, as of 2017: vmFork did not work for RDSH/multi-session workloads (single-user desktops only), only 'floating' assignment was supported (desktops randomly assigned), and Instant Clone desktops could not have a persistent disk. Patching is push-image based: update the golden/parent image, force users to log out and back in, and they land on the latest patched clone. Bas's practical add: combine Instant Clones with a layering / environment-management product (Unidesk/App Layering, VMware App Volumes, UEM, Citrix WEM/Norskale) and 'non-persistent will feel persistent -- the best of both worlds.'

*Bron: blogpost 'VMware's Instant Clones technology with a touch of XenDesktop' (2017-01-17), basvankaam.com.*

## Verwante notities

- [How application layering works: filter drivers merging virtual disks](how-application-layering-works-2.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [Non-persistent plus layering = the best of both worlds](non-persistent-feels-persistent-with-layering.md)
- [Pooled vs dedicated desktops: the durable trade-off](pooled-vs-dedicated-desktops.md)
- [PVS vs MCS image-delivery tradeoffs (XenDesktop 7 era)](pvs-vs-mcs-tradeoffs.md)
- [How VMware Instant Clones (vmFork) provision desktops in seconds](vmware-instant-clones-vmfork-mechanics.md)
