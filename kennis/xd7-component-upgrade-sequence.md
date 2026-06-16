---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, pvs, storefront, upgrade]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenDesktop 7 component upgrade sequence and what is excluded

How it worked then: the XD7 installer ran an in-place upgrade that auto-detected and upgraded license servers, Delivery Controllers, Studio, Director, Desktop OS VDAs and optionally Citrix Receiver. The Site database was upgraded last, automatically or manually, from an XD7 Studio installation.

Key gotchas:
- PVS, SCVMM and StoreFront were NOT part of the in-place upgrade and had to be updated separately. PVS servers should be upgraded before the XD Site, and PVS 7 could not create new desktops against XD5.x controllers.
- Studio and Director, when installed separately on a management machine, had to be upgraded separately; side-by-side Studio installations were not supported.
- With multiple controllers you could upgrade one or two first so users kept working, with a brief interruption during the final database upgrade.
- VDAs on Windows XP or Windows Vista could not be upgraded to version 7 VDAs; a separate installer pushed them to the latest supported VDA for that OS, and they ran in the XD7 Site with reduced feature support.

Always back up the Site database before upgrading anything.

*Bron: blogpost 'Upgrade and or migrate to XD7. What's involved?!' (2013-08-12), basvankaam.com.*

## Verwante notities

- [XenApp migration tooling: Migration Center and 6.0-to-6.5 Upgrade Utility (2013)](xenapp-migration-tooling-2013.md)
