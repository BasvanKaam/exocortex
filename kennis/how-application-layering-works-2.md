---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [application-layering, filter-driver, vhd, vmdk, in-guest-mount, unidesk, app-volumes, app-disks]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How application layering works: filter drivers merging virtual disks

How it worked then (2015), across vendors (UniDesk, VMware App Volumes, Citrix AppDisks, Liquidware, FSLogix): an application is installed/captured onto a virtual hard disk (VHD or VMDK). That disk is mounted onto a VM (assigned per-user or per-machine, varies by product); some products also support an in-guest mount so layers can reach physical machines too. A mini filter driver (write filter) in the base OS sits over the file system and seamlessly merges every mounted layer into c:\ so apps appear locally installed, including .ini, .dll, registry entries and other files. Calls to the file system (e.g. launching an app) get filtered and redirected to the right layer/VHD. Trade-offs vs app virtualization: it adds another product and interface to learn, has licensing cost, and apps are not isolated the way virtualized apps are.

*Bron: blogpost 'Application Layering questions? I got answers. Graphical cheat sheet included!' (2015-12-01), basvankaam.com.*

## Verwante notities

- [In-guest vs hypervisor-level mounting in application layering](app-layering-in-guest-mounting-explained.md)
- [Framing: keep application layering and application virtualization distinct](app-layering-not-app-virtualization.md)
- [Application layering complements, does not replace, app virtualization](application-layering-vs-virtualization.md)
- [Citrix acquired Unidesk to own application layering](citrix-acquires-unidesk-layering.md)
- [FlexApp 6.5: filter drivers replace symbolic links, broadening layering support](flexapp-filter-driver-vs-symbolic-links.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
- [Instant Clones are for non-persistent floating VDI only](instant-clones-use-case-and-limits.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
