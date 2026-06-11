---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vdi, pooled, dedicated, persistent, image-management]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Pooled vs dedicated desktops: the durable trade-off

A concept Bas returns to repeatedly. All VDI VMs are provisioned from a master / golden image, so they start identical.

- Pooled: all changes to the OS are discarded on log-off or reboot. The VM returns clean to the pool for reuse. Installed apps, updates and personal settings vanish, so you need a good user-profile solution. Storage can be under-committed (with a daily reboot schedule) because differencing disks rarely grow far in a day.
- Dedicated / persistent: changes are preserved across reboot; the VM is bound to one user. Differencing disk keeps growing until full, so no under-committing, size accordingly, and it costs more IOPS and storage.

Management catch with dedicated: you cannot update the base master image without destroying the differencing disk, so each desktop must be managed individually. Pooled lets you update the base image, reassign, reboot and go.

*Bron: blogpost 'VDI, storage and the IOPS that come with it. Part 1 & 2.' (2013-11-12), basvankaam.com.*

## Verwante notities

- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [Instant Clones are for non-persistent floating VDI only](instant-clones-use-case-and-limits.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [If most VDIs are non-persistent, why aren't more apps virtualised?](non-persistent-vs-app-virtualisation-surprise.md)
- [Personal vDisk: persistence of dedicated, manageability of pooled](personal-vdisk-pvd-concept.md)
- [Positie: Personal vDisk is great and underappreciated](positie-pvd-underappreciated.md)
- [Categorize users before choosing a desktop model](user-categorization-for-desktop-design.md)
- [VDI is more romantic on paper than in reality](vdi-romantic-vs-reality-position.md)
- [The five VDI workload phases and boot/logon storms](vdi-workload-phases-storms.md)
