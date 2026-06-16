---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenapp, migration, tool, powershell]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenApp migration tooling: Migration Center and 6.0-to-6.5 Upgrade Utility (2013)

Three Citrix tools for moving Farm objects:
- XenApp 6.0 Migration Tool (CTX125471): command-line only, migrates 4.5/5.0 (at HRP5) settings to a 6.0 Farm.
- XenApp 6.5 Migration Center: more advanced, has a GUI, supports an Analyze/dry-run, and can map source servers to worker groups. Used for 4.5/5.0/6.0 -> 6.5.
- XenApp 6.0 to 6.5 Upgrade Utility (CTX130614): a customisable script that silently uninstalls 6.0 components in the correct order, installs 6.5 and by default joins the server to an existing 6.5 Farm as a worker, then verifies the IMA service is running. Requires UAC off and PowerShell execution policy Unrestricted. Takes ~30 minutes and several reboots.

Clever combined workflow Bas describes: migrate all published-app configurations with the Migration Center, then run the Upgrade Utility in place on the boxes that hold the actual application bits - so you don't have to reconfigure 'horror apps' by hand.

*Bron: blogpost 'End of Life... to Migrate or not to Migrate?' (2013-04-28), basvankaam.com.*

## Verwante notities

- [Citrix IMA Architecture: Data Store and Local Host Cache](citrix-ima-architecture.md)
- [What FMA 7.6 changed vs IMA: LHC gone, MCS for servers, Connection Leasing](fma-76-migration-improvements.md)
- [XenDesktop 7 component upgrade sequence and what is excluded](xd7-component-upgrade-sequence.md)
- [Upgrade vs migrate to XenDesktop 7: two different paths](xd7-upgrade-vs-migrate.md)
- [XenApp Farms must be migrated in parallel, not upgraded in place (2013)](xenapp-no-in-place-upgrade-build-in-parallel.md)
