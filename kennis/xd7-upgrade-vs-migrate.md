---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, migration, upgrade]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Upgrade vs migrate to XenDesktop 7: two different paths

How it worked then (XenDesktop 7 era, 2013): in-place upgrade and migration were distinct operations with different prerequisites.

- An in-place upgrade to a XenDesktop 7 Site was only possible from a XenDesktop 5.x Site. The XD4 migration tool could not export/import XD5 data; you had to upgrade in place.
- A XenDesktop 4.x Farm had no in-place upgrade path. You had to use the migration tool (Export tool XdExport, an XML editor for XdSettings.xml, and Import tool XdImport running Import-XdSettings.ps1).
- You could not upgrade from XenDesktop Express Edition; a VDI, Enterprise or Platinum license was required first.
- For migration, both environments had to run the same hypervisor version and Active Directory environment, and XD4 VDAs first had to be brought to XD5.x level so they were compatible with both XD4 and XD7 controllers.

At the time of writing Citrix had announced there was no upgrade or migration path for existing XenApp 6.5 customers yet; a toolset of scripts was promised for a future release.

*Bron: blogpost 'Upgrade and or migrate to XD7. What's involved?!' (2013-08-12), basvankaam.com.*
