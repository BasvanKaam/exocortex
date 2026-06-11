---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [nutanix, data-locality, shadow-clones, cvm, vdi, hyperconverged]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Nutanix data locality and shadow clones for VDI

How it worked (2015), but the concepts are durable hyperconverged storage primitives:

- Each cluster node runs a hypervisor (Acropolis/AHV, Hyper-V or ESXi) hosting a Controller VM (CVM) where the storage intelligence lives. Data locality means a VM's reads and writes are served by the CVM on the same physical node, and the VM's data is physically stored on that node's local SSDs/HDDs. When a VM moves to another node, I/O is immediately handled by the new local CVM and the data is silently migrated to follow it.

- Shadow clones cache read-only disks (a VMware View replica disk or a Citrix MCS master VM disk) locally on each CVM serving read requests for that disk, so a linked clone's reads to the base image stay node-local. Nutanix auto-identifies read-only shared disks by monitoring vDisk access patterns.

- Data tiering / disk balancing moves the coldest data off local SSDs (first to other SSDs in the cluster, then to HDDs once the SSD tier hits a threshold) to keep hot data on fast local media. These mechanics are why MCS/PVS VDI workloads perform well on hyperconverged platforms.

*Bron: blogpost 'Nutanix & Citrix… A match made in heaven' (2015-09-25), basvankaam.com.*

## Verwante notities

- [Nutanix Acropolis is three components, not just a hypervisor](nutanix-acropolis-three-components.md)
- [Nutanix AFS folds the file server into the HCI cluster](nutanix-afs-scale-out-file-services.md)
- [How VMware Instant Clones (vmFork) provision desktops in seconds](vmware-instant-clones-vmfork-mechanics.md)
