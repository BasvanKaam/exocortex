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

- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [In-guest vs hypervisor-level mounting in application layering](app-layering-in-guest-mounting-explained.md)
- [Application delivery: layering vs virtualisation, and AppDisks](application-delivery-layering-vs-virtualisation.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Application layering vendor landscape circa 2016](application-layering-vendor-landscape-2016.md)
- [Bas's key takeaways on application delivery and layering](bas-key-takeaways-application-delivery.md)
- [Bas's questions before choosing a layering solution](bas-layering-questions-to-ask.md)
- [Bas: only ~50-60% of apps can be virtualised](bas-on-virtualisation-coverage-50-60-percent.md)
- [Bas on the pros of application layering](bas-pros-of-application-layering.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [Citrix acquired Unidesk to own application layering](citrix-acquires-unidesk-layering.md)
- [Citrix AppDisks: application layering for golden images](citrix-appdisks-application-layering.md)
- [Citrix AppDisks was built on PvD and shipped machine-only first](citrix-appdisks-pvd-roots.md)
- [How application layering works: filter drivers merging virtual disks](how-application-layering-works-2.md)
- [Bas on MCS, workloads and the case for application layering](mcs-application-workloads-layering.md)
