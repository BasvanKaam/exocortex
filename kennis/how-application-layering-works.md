---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [application-layering, filter-drivers, filter-driver, vhd, vmdk, in-guest-mount, unidesk, app-volumes, app-disks]
layer: reference
bron: inside-citrix-fma
---

# How application layering works (filter drivers)

Application layering (distinct from application virtualisation) works roughly like this: an application is first installed/captured onto a VHD or VMDK virtual hard disk. That virtual disk is then mounted onto a virtual machine (assigned to a user or machine, depending on the solution). An in-guest mount is sometimes optional, making layers available to physical machines too.

Almost all layer vendors use (mini-) filter drivers, a.k.a. write filters, residing in the base OS to manage the file system. These filters seamlessly merge mounted application layers into the file system (c:\) so they appear locally installed (including .ini, .dll, registry entries, etc.). When an application launches, calls to the file system are filtered and directed to the appropriate application layer (VHD/VMDK).

How it worked then (2015), across vendors (UniDesk, VMware App Volumes, Citrix AppDisks, Liquidware, FSLogix): the mechanics above held for every product, with disk assignment per-user or per-machine varying by product.

Trade-offs vs app virtualisation: layering adds another product and interface to learn, has licensing cost, and apps are not isolated the way virtualised apps are.

*Bron: blogpost 'Application Layering questions? I got answers. Graphical cheat sheet included!' (2015-12-01), basvankaam.com.*
