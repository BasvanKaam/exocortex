---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [pvs, provisioning-services, vdisk, best-practices, rdsh]
layer: rich
bron: inside-citrix-fma
---

# Bas's PVS key takeaways and best-practice asides

From Bas's PVS chapter wrap-up, with his characteristic practical framing:

- PVS streams a base image over the network to virtual or physical machines, for both desktop and server OSes. A device using a vDisk is a Target Device; the machine used to create/maintain the vDisk is the Master Target Device; Target Devices are managed in Device Collections; dozens, hundreds or thousands can share a single vDisk.
- The vDisk life cycle is creation, deployment, maintenance and retirement, leveraging the built-in PVS Versioning mechanism.
- "Give your write cache sizing and location some consideration: you will be glad that you did."
- Private Mode (where changes to the vDisk are saved) exists but isn't a popular approach.
- His reassurance: PVS can seem complicated at first; take it step by step, you'll be fine.
- Make your PVS infrastructure highly available.
- On Personal vDisks (PvDs): apply them wisely, it's not for everyone. And, somewhat off topic, in many cases where VDI is considered, **RDSH might make more sense**.
- On the physical-vs-virtual debate: it used to be best practice to use physical machines for Provisioning Servers, but today Citrix almost always recommends virtual machines, thanks to networking enhancements. The same applies to isolating PVS traffic, now mainly only justified by security considerations. "Keep it simple."
- Reference articles he cites: CTX117372 (PVS networking best practices), CTX131611 (known hardware-related PVS issues), CTX124185 (antivirus best practices on PVS vDisks).

## Verwante notities

- [Bas's PVS recommendation: hybrid versioning approach](bas-pvs-hybrid-versioning-recommendation.md)
- [MCS rollbacks and reboot considerations (boot storms, disconnect policies)](mcs-rollbacks-and-reboot-considerations.md)
- [Provisioning Services essentials and Bas's advice](provisioning-services-essentials.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS high availability](pvs-high-availability.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [PVS vDisk versioning and lifecycle](pvs-vdisk-versioning-lifecycle.md)
- [PVS write cache options](pvs-write-cache-options.md)
