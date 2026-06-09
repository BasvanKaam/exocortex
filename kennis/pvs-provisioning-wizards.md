---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, provisioning-wizard, device-collection, xendesktop]
layer: reference
bron: inside-citrix-fma
---

# PVS provisioning wizards: streamed VM and XenDesktop setup

Once the PVS infrastructure, Master Target Device and a vDisk exist, you auto-provision target devices with one of two wizards. The devices that end up using a vDisk are grouped into **device collections**.

**Streamed VM setup wizard** (from the PVS console): creates multiple virtual target devices from a preconfigured template VM, creates target device objects in the appropriate (existing) device collection, and assigns a Standard Image Mode vDisk. It supports XenServer, Hyper-V (via SCVMM) and ESX (via vCenter). During the wizard you pick the hypervisor, the VM template, the device collection, the number of VMs, CPU and memory per VM, and whether to create new or use existing AD computer accounts.

**XenDesktop setup wizard:** requires Delivery Controllers and Provisioning Servers on the **same version**. It creates VMs on a XenDesktop Host Connection hypervisor from a template, creates target devices in a new/existing device collection named after the XenDesktop Catalog, assigns a Standard Image vDisk, and adds the desktops to the Machine Catalog in Studio. Steps it performs: create a Machine Catalog if needed; create VMs from the template; create BDM partitions if specified; for a Streamed-with-personal-vDisk Catalog create and attach a PvD; create a write cache disk of the specified size; create PVS target devices and assign the vDisk; add devices to the PVS collection; add VMs to the Catalog; boot each VM to format the write cache disk.
