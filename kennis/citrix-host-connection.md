---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, host-connection, hypervisor, mcs, studio]
layer: reference
bron: inside-citrix-fma
---

# Citrix Host Connection

A **Host Connection** is a bridge from Citrix Studio to the underlying hypervisor or cloud platform where your VMs reside, enabling Studio to start, stop, create, delete and monitor VMs via the platform's APIs. It is configured during initial Site setup or later under Configuration > Hosting in Studio.

Supported targets: VMware vSphere, Microsoft Hyper-V, Citrix XenServer, Amazon Web Services, Microsoft Azure and Citrix CloudPlatform (with the Nutanix Acropolis Hypervisor announced to be added shortly). For hypervisors you point at the management layer: **SCVMM** for Hyper-V, **Virtual Center** for VMware, **XenCenter** for XenServer — though with XenServer a standalone host or Poolmaster is technically sufficient.

A Host Connection is optional, but without one you lose VM auto-provisioning: no MCS-based pooled or dedicated Catalogs, and the Machine Catalog wizard offers only physical hardware (MCS greyed out; PVS and 'another service or technology' still selectable). Notably, the **PVS management console can still provision VMs without a Host Connection**, because PVS can talk directly to vCenter and/or the vSphere host.
