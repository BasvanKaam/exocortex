---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvd, personal-vdisk, pvs, mcs, persistence]
layer: reference
bron: inside-citrix-fma
---

# Personal vDisks (PvD)

A **Personal vDisk (PvD)** lets users store their changes when working on a virtual, pooled static machine, combining the persistence of dedicated desktops with the management advantages of pooled desktops. It can be used with both PVS and MCS, but only assigned to a **desktop OS** (server OSs not supported), and with PVS only to virtual machines (not physical).

You keep one base (master) image and attach an extra PvD per VM storing all personal changes: file and registry changes, apps installed/streamed via SCCM/App-V/XenApp, wallpapers, Start menu, favourites — basically everything under C:\Users plus installed/updated applications. A XenDesktop **PvD agent** on the master image tracks base-image vs PvD content and blends them after the base image is updated and rolled out (which still requires a VM reboot).

By default the PvD VHD is split 50/50 between profile/personal storage and application installs (e.g. 5 GB + 5 GB on a 10 GB PvD); a registry setting can change this to 70/30, 90/10 or 99/1. If a conflict occurs (user installs the same app as the admin puts on the base image), the system removes the user's copy to keep the PvD small (default, customisable). PvDs support thin provisioning and can sit on different storage than the VMs to spread IOPS; they're compatible with most profile management and PC lifecycle tools (SCCM) and app virtualization (XenApp), and are also available in VDI-in-a-Box.

Citrix advises PvDs for no more than ~100 to 125 machines to avoid complexity; beyond that, use fully cloned VMs. Bas considers persistent desktops via PvD/PVS uncommon in larger enterprises but popular with smaller companies, and includes it because he gets many questions about it.

## Verwante notities

- [Bas's questions before choosing a layering solution](bas-layering-questions-to-ask.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [MCS desktop types: Pooled-Random, Pooled-Static, Dedicated](mcs-desktop-types.md)
- [MCS Differencing Disk and Identity Disk](mcs-differencing-and-identity-disk.md)
- [Bas's PVS key takeaways and best-practice asides](provisioning-services-key-takeaways.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS provisioning wizards: streamed VM and XenDesktop setup](pvs-provisioning-wizards.md)
- [PVS vDisk creation, Standard vs Private Image Mode](pvs-vdisk-standard-vs-private-image-mode.md)
- [PVS write cache options](pvs-write-cache-options.md)
- [VDA install options and supported operating systems](vda-install-options-and-supported-os.md)
