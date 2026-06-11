---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [nutanix, acropolis, ahv, app-mobility-fabric, distributed-storage-fabric, prism]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Nutanix Acropolis is three components, not just a hypervisor

Clarification Bas pushed in 2015: people kept calling Acropolis 'a new hypervisor', but Acropolis is three parts:

1. Acropolis Hypervisor (AHV) - a Nutanix-native hypervisor based on Linux KVM, free of charge, shipped by default, supporting Windows/SUSE/CentOS/Ubuntu guests. (The free Nutanix Community Edition also runs AHV.) It was the latest addition to the Citrix Certified portfolio.
2. App Mobility Fabric - mostly work-in-progress at the time: intelligent VM placement, cross-hypervisor and hypervisor-to-cloud migration, cross-hypervisor HA/DR. AHV was to be the first hypervisor to fully support it.
3. Distributed Storage Fabric - the distributed software storage (compression, snapshots, clones, HA/DR, dedupe, data tiering) that eliminates traditional SAN/NAS.

PRISM is the single management GUI on top. 'Extreme Computing Platform' was a marketing term combining Acropolis + Prism. As of late 2015, AHV VMs could be manually added to a XenDesktop catalog (Citrix-supported); a native Host Connection for MCS provisioning was still in the making.

*Bron: blogpost 'Nutanix & Citrix… A match made in heaven' (2015-09-25), basvankaam.com.*

## Verwante notities

- [Citrix Validated Solution: XenDesktop on Nutanix reference architecture](citrix-validated-solution-nutanix.md)
- [Nutanix AFS folds the file server into the HCI cluster](nutanix-afs-scale-out-file-services.md)
- [Nutanix architecture: nodes and Controller VMs](nutanix-controller-vm-architecture.md)
- [Converged (hyperconverged) infrastructure collapses compute and storage into one appliance](nutanix-converged-infrastructure-concept.md)
- [Nutanix data locality and shadow clones for VDI](nutanix-data-locality-shadow-clones.md)
- [How Nutanix NOS 4.0 worked: Prism Central, integrated data protection, one-click upgrade](nutanix-nos-4-features-2014.md)
- [Nutanix's 'new' platform names are partly rebrands of tech they already had](positie-nutanix-rebrands-existing-tech.md)
