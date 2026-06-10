---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, terminology, farm, device-collection]
layer: reference
bron: inside-citrix-fma
---

# PVS terminology: Farm, Site, Store, Device Collection, Target Device

Core Provisioning Services terms:

- **Farm:** the top level of a PVS infrastructure. All sites within a Farm share that Farm's Microsoft SQL database. A Farm also includes a Citrix License Server, local or network-shared storage, and collections of target devices.
- **Site:** a logical grouping of all Provisioning Servers, Device Collections, target devices and storage.
- **Stores:** where vDisk files are physically stored — local storage on the PVS server(s) or shared storage (SAN). When you create a vDisk you assign it to a store.
- **Device Collections:** let you manage many devices as a logical group, simplifying administration (tasks run at collection level rather than per device). A collection can also represent a physical location or a specific subnet range.
- **Target Devices:** all virtual and physical devices that get a vDisk streamed over the network. The device used to create and maintain the vDisk is the **Master Target Device**.

## Verwante notities

- [Provisioning Services essentials and Bas's advice](provisioning-services-essentials.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS boot mechanism: Bootstrap, TFTP and BDM](pvs-boot-mechanism-bootstrap-tftp-bdm.md)
- [PVS high availability](pvs-high-availability.md)
- [PVS provisioning wizards: streamed VM and XenDesktop setup](pvs-provisioning-wizards.md)
- [PVS vDisk creation, Standard vs Private Image Mode](pvs-vdisk-standard-vs-private-image-mode.md)
