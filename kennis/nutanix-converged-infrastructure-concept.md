---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [nutanix, converged-infrastructure, storage, web-scale, datacenter]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Converged (hyperconverged) infrastructure collapses compute and storage into one appliance

The Nutanix Virtual Computing Platform converges compute and storage into a single system, removing the need for a traditional SAN or NAS. A single 2U appliance can hold up to four independent nodes (blade-like), each with its own compute, memory and storage, each running an industry-standard hypervisor.

The key idea: all control logic lives in intelligent VMs (Nutanix calls them controller VMs / CVMs) that run on each node and handle I/O for the local hypervisor. A global storage pool aggregates capacity from all nodes; every host in the cluster can access it. Storage is exposed to the hypervisor through standard interfaces (NFS, iSCSI) so existing Ethernet networking is reused. Intelligence is abstracted into a distributed software layer rather than baked into specialized hardware. The modular building-block design lets you start with two or three nodes and scale out incrementally, avoiding a large upfront SAN investment.

This is the durable architectural concept behind hyperconvergence, even though the specific product/version here (NOS 4.0, 2014) is dated.

*Bron: blogpost 'Introducing Nutanix OS (NOS) 4.0... What's new?!' (2014-04-15), basvankaam.com.*

## Verwante notities

- [Bas leans into hyper-convergence and web-scale as the future](bas-on-web-scale-as-future-of-it.md)
- [Citrix Validated Solution: XenDesktop on Nutanix reference architecture](citrix-validated-solution-nutanix.md)
- [What a converged infrastructure is](converged-infrastructure-definition.md)
- [HP Moonshot is converged but not truly web-scale](hp-moonshot-is-not-web-scale.md)
- [Hyperconverged Infrastructure: Three Use Cases](hyperconverged-three-use-cases.md)
- [Loose coupling as a core Cloud design principle](loose-coupling-cloud-architecture.md)
- [Nutanix Acropolis is three components, not just a hypervisor](nutanix-acropolis-three-components.md)
- [Nutanix AFS folds the file server into the HCI cluster](nutanix-afs-scale-out-file-services.md)
- [Plenty of room left for innovation in HCI, GPU and app delivery (2015)](room-for-innovation-hci-gpu-app-delivery.md)
- [Web-scale architecture: software-defined, scale-out, self-healing on x86](web-scale-architecture-principles.md)
