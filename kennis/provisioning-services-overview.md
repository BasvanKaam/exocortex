---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, single-image-management, vdisk, streaming]
layer: reference
bron: inside-citrix-fma
---

# Citrix Provisioning Services (PVS) overview

For delivering the base OS in Citrix environments you can install/manage manually, automate/script installs, or use **single image management** via Machine Creation Services (MCS) or **Provisioning Services (PVS)**.

PVS is based on **software streaming**: a single read-only **vDisk** (virtual disk) is streamed over the network to many **target devices** (XenApp servers or XenDesktop VDI VMs). You always run at least two provisioning servers for HA, more depending on scale. Just two provisioning servers can provision several hundred or even thousands of physical/virtual machines (though more is preferred).

MCS will be discussed in the next chapter; the PVS chapter is meant as a high-level overview rather than a full setup/management guide.

## Verwante notities

- [Bas's PVS recommendation: hybrid versioning approach](bas-pvs-hybrid-versioning-recommendation.md)
- [Citrix Project Accelerator: web-based design guidance](citrix-project-accelerator.md)
- [FlexCast delivery technology, worker types and delivery models](flexcast-delivery-models-and-worker-types.md)
- [Host Connection key takeaways: MCS/PVS and cloud support](host-connection-mcs-pvs-cloud-support-key-takeaways.md)
- [Host Connections now support cloud, not just hypervisors](host-connections-cloud-support.md)
- [Machine Creation Services essentials](machine-creation-services-essentials.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [Provisioning Services essentials and Bas's advice](provisioning-services-essentials.md)
- [Bas's PVS key takeaways and best-practice asides](provisioning-services-key-takeaways.md)
- [PVS boot mechanism: Bootstrap, TFTP and BDM](pvs-boot-mechanism-bootstrap-tftp-bdm.md)
- [PVS high availability](pvs-high-availability.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [PVS provisioning wizards: streamed VM and XenDesktop setup](pvs-provisioning-wizards.md)
- [PVS terminology: Farm, Site, Store, Device Collection, Target Device](pvs-terminology-farm-site-store-collection.md)
- [PVS vDisk creation, Standard vs Private Image Mode](pvs-vdisk-standard-vs-private-image-mode.md)
- [PVS vDisk versioning and lifecycle](pvs-vdisk-versioning-lifecycle.md)
- [PVS write cache options](pvs-write-cache-options.md)
