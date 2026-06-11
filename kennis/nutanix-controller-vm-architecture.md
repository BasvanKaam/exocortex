---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [nutanix, hci, controller-vm, storage, hypervisor]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Nutanix architecture: nodes and Controller VMs

How it worked then (2014): the Nutanix Virtual Computing Platform converged compute and storage into a single system, eliminating the need for traditional NAS or SAN arrays. A single 2U appliance could hold up to four independent nodes (blade-like), each with its own compute, memory and storage and running an industry-standard hypervisor. The control logic was embedded into intelligent Controller VMs running on each node, handling all I/O for the local hypervisor ("this is where the magic happens"). A global storage pool aggregated capacity across all nodes, exposed to the hypervisor through traditional interfaces like NFS and iSCSI, and ran over existing Ethernet networking. Storage and networking being local to the VMs was the big performance draw, with scale-on-demand removing over-provisioning.

*Bron: blogpost 'Last week Nutanix opened their Dutch HQ and I was there, here are my thoughts.' (2014-02-24), basvankaam.com.*

## Verwante notities

- [Citrix Validated Solution: XenDesktop on Nutanix reference architecture](citrix-validated-solution-nutanix.md)
- [What a converged infrastructure is](converged-infrastructure-definition.md)
- [Nutanix Acropolis is three components, not just a hypervisor](nutanix-acropolis-three-components.md)
- [Nutanix AFS folds the file server into the HCI cluster](nutanix-afs-scale-out-file-services.md)
