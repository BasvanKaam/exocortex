---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [pvs, provisioning-services, vdisk, write-cache, bdm]
layer: rich
bron: inside-citrix-fma
---

# Provisioning Services essentials and Bas's advice

PVS streams a base image over the network to virtual or physical machines, for both desktop and server OSs. A device using a vDisk is a Target Device; the machine that creates/maintains the vDisk is the Master Target Device; Target Devices are managed via Device Collections, and dozens to thousands can share one vDisk. The vDisk life cycle is creation, deployment, maintenance and retirement, handled via PVS Versioning.

Bas's hard-won advice: PVS can seem complicated at first — take it step by step and you'll be fine. Give write cache sizing and location real thought. Make PVS highly available. Today Citrix almost always recommends virtual machines for Provisioning Servers (thanks to networking enhancements), and traffic isolation is now mainly justified by security rather than performance — keep it simple. The BDM boot method cuts boot times by roughly 5-10 seconds by skipping PXE and TFTP. When vDisks are stored locally, replicate them (DFS-R or Robocopy recommended); be aware promoting a version opens and writes to the vDisk, risking inconsistencies. PvDs (Personal vDisks) have their use but apply them wisely — and in many cases where VDI is considered, RDSH might make more sense.

## Bron-citaten (NL, verbatim)

> While PvDs have their use, apply them wisely: it's not for everyone.

## Verwante notities

- [Bas's PVS recommendation: hybrid versioning approach](bas-pvs-hybrid-versioning-recommendation.md)
- [Bas's PVS key takeaways and best-practice asides](provisioning-services-key-takeaways.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS boot mechanism: Bootstrap, TFTP and BDM](pvs-boot-mechanism-bootstrap-tftp-bdm.md)
- [PVS high availability](pvs-high-availability.md)
- [PVS terminology: Farm, Site, Store, Device Collection, Target Device](pvs-terminology-farm-site-store-collection.md)
- [PVS write cache options](pvs-write-cache-options.md)
