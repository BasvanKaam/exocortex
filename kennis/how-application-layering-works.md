---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [application-layering, filter-drivers, vhd, vmdk]
layer: reference
bron: inside-citrix-fma
---

# How application layering works (filter drivers)

Application layering (distinct from application virtualisation) works roughly like this: an application is first installed/captured onto a VHD or VMDK virtual hard disk. That virtual disk is then mounted onto a virtual machine (assigned to a user or machine, depending on the solution). An in-guest mount is sometimes optional, making layers available to physical machines too.

Almost all layer vendors use (mini-) filter drivers, a.k.a. write filters, residing in the base OS to manage the file system. These filters seamlessly merge mounted application layers into the file system so they appear locally installed (including .ini, .dll, registry entries, etc.). When an application launches, calls to the file system are filtered and directed to the appropriate application layer (VHD/VMDK).

## Verwante notities

- [Application delivery: layering vs virtualisation, and AppDisks](application-delivery-layering-vs-virtualisation.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Bas's key takeaways on application delivery and layering](bas-key-takeaways-application-delivery.md)
- [Bas's questions before choosing a layering solution](bas-layering-questions-to-ask.md)
- [Bas: only ~50-60% of apps can be virtualised](bas-on-virtualisation-coverage-50-60-percent.md)
- [Bas on the pros of application layering](bas-pros-of-application-layering.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [Citrix AppDisks: application layering for golden images](citrix-appdisks-application-layering.md)
- [Bas on MCS, workloads and the case for application layering](mcs-application-workloads-layering.md)
