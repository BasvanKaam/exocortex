---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [application-layering, fslogix, app-volumes, liquidware, vhd-vmdk]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# In-guest vs hypervisor-level mounting in application layering

How it worked then (2017, cheat sheet v3.0): 'in-guest Windows' mounting means mounting a VHD or VMDK file directly into the Windows file system / OS, as opposed to mounting at the hypervisor level. FSLogix App Containers mounted all virtual disks in-guest exclusively. Liquidware Labs Flex Apps mounted VHD files in-guest but mounted VMDK files (on VMware) at the hypervisor level. App Volumes used VHD to mount in-guest for physical machines.

The practical consequence Bas highlighted: in-guest mounting is what makes supporting physical (non-virtual) machines possible. Separately, App Volumes Writeable Volumes could store user profile data, user-installed applications, or both, but did not work on RDSH deployments.

He also noted FSLogix is not strictly an application layering technology, but solved adjacent problems elegantly enough to belong on the sheet.

*Bron: blogpost 'The application layering technology cheat sheet, version 3.0!' (2017-02-28), basvankaam.com.*

## Verwante notities

- [Application layering narrows to the big three (2017)](app-layering-big-three-2017.md)
- [Application layering vendor landscape circa 2016](application-layering-vendor-landscape-2016.md)
- [FlexApp 6.5: filter drivers replace symbolic links, broadening layering support](flexapp-filter-driver-vs-symbolic-links.md)
- [FSLogix is not an application layering company; App Disks are doomed](fslogix-not-an-app-layering-company.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
- [How application layering works: filter drivers merging virtual disks](how-application-layering-works-2.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
