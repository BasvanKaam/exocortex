---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, pvd, vdi, personalization, xendesktop]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Personal vDisk: persistence of dedicated, manageability of pooled

How it worked then: Personal vDisk (PvD, introduced in XenDesktop 5.6, improved in XD7) attached an extra per-user persistent disk to a pooled-with-PvD VM. The PvD stored all file-level and registry changes, the user profile under C:\Users, and user-installed/streamed apps (SCCM, App-V cache, XenApp), while the base image stayed shared and centrally managed.

Mechanics and characteristics:
- A PvD agent on the master image tracked what was on the base image versus the PvD and blended the two, so admins could update the base image and have user changes persist on top after a reboot/rollout.
- The PvD VHD defaulted to a 50/50 split between profile data and app installs; this was registry-adjustable to 70/30, 90/10 or 99/1, important when combined with profile management or folder redirection.
- On conflict (user installs the same app the admin adds to the base), the default behaviour removed the user copy to keep the PvD small.
- PvDs supported thin provisioning, could live on different storage from the VM to spread IOPS, and ended up smaller than dedicated differencing disks.

The value proposition: pooled-style management and storage with dedicated-style persistence. This was Bas's first deep dive into a pre-XD7 feature he found underused.

*Bron: blogpost 'XenDesktop (MCS) Personal vDisks' (2013-09-22), basvankaam.com.*

## Verwante notities

- [App Disks and PvD never took off; Unidesk was the right call](app-disks-and-pvd-never-took-off.md)
- [Citrix AppDisks was built on PvD and shipped machine-only first](citrix-appdisks-pvd-roots.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [Non-persistent plus layering = the best of both worlds](non-persistent-feels-persistent-with-layering.md)
- [Pooled vs dedicated desktops: the durable trade-off](pooled-vs-dedicated-desktops.md)
- [Positie: Personal vDisk is great and underappreciated](positie-pvd-underappreciated.md)
- [Features Server VDI cannot do](server-vdi-unsupported-features.md)
- [VDI-in-a-Box: the simplified all-in-one VDI appliance](vdi-in-a-box-architecture.md)
- [How VMware Instant Clones (vmFork) provision desktops in seconds](vmware-instant-clones-vmfork-mechanics.md)
