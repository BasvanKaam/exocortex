---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [application-layering, filter-driver, vhd, vmdk, in-guest-mount, unidesk, app-volumes, appdisks]
layer: reference
bron: inside-citrix-fma
---

# How application layering works (filter drivers)

Application layering (distinct from application virtualisation) works roughly like this: an application is first installed/captured onto a VHD or VMDK virtual hard disk. That virtual disk is then mounted onto a virtual machine (assigned to a user or machine, depending on the solution). An in-guest mount is sometimes optional, making layers available to physical machines too.

Almost all layer vendors use (mini-) filter drivers, a.k.a. write filters, residing in the base OS to manage the file system. These filters seamlessly merge mounted application layers into the file system (c:\) so they appear locally installed (including .ini, .dll, registry entries, etc.). When an application launches, calls to the file system are filtered and directed to the appropriate application layer (VHD/VMDK).

How it worked then (2015), across vendors (UniDesk, VMware App Volumes, Citrix AppDisks, Liquidware, FSLogix): the mechanics above held for every product, with disk assignment per-user or per-machine varying by product.

Trade-offs vs app virtualisation: layering adds another product and interface to learn, has licensing cost, and apps are not isolated the way virtualised apps are.

*Bron: blogpost 'Application Layering questions? I got answers. Graphical cheat sheet included!' (2015-12-01), basvankaam.com.*

## Verwante notities

- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [In-guest vs hypervisor-level mounting in application layering](app-layering-in-guest-mounting-explained.md)
- [Application layering vendor landscape circa 2016](application-layering-vendor-landscape-2016.md)
- [Application layering complements, does not replace, app virtualization](application-layering-vs-virtualization.md)
- [Citrix acquired Unidesk to own application layering](citrix-acquires-unidesk-layering.md)
- [Citrix AppDisks: application layering for golden images](citrix-appdisks-application-layering.md)
- [FlexApp 6.5: filter drivers replace symbolic links, broadening layering support](flexapp-filter-driver-vs-symbolic-links.md)
