---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [xenapp, fma, ima, migration, connection-leasing]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# What FMA 7.6 changed vs IMA: LHC gone, MCS for servers, Connection Leasing

How it worked then (2015). Moving from XenApp 6.5 (IMA) to XenApp/XenDesktop 7.6 (FMA) brought concrete architectural changes:

- Machine Creation Services (MCS) could now provision server OS (server VDA), not just desktop OS; PVS still worked and you could mix MCS and PVS. PVS 7.6 added cache-in-RAM with spillover to disk.
- The Local Host Cache (LHC) and zones were removed. Connection Leasing replaced part of LHC's role: recently launched (default last two weeks, configurable) assigned applications/desktops stay accessible when the central Site database is down. Resources must be assigned for it to work, so it doesn't cover pooled desktops.
- Only SQL Server is supported for the central Site database. For small HSD-only deployments, SQL HA is no longer strictly needed.
- All servers are workers only (lightweight install) by default: no more elections, no per-server config replication, less IMA traffic overhead.
- SSL/TLS (FIPS AES) is integrated into the core of the VDA, removing the need for SSL Relay or IPSec.
- FMA is said to scale ~10% more efficiently than IMA (higher session density on the same hardware).
- No need to install Remote Desktop Services on Delivery Controllers, unlike 6.5 Data Collectors. Different server/desktop OS versions can coexist in one Site.

*Bron: blogpost 'The glass is half full... 50+ reasons why I think it might be time to move to XenApp 7.6!' (2015-04-12), basvankaam.com.*

## Verwante notities

- [How Connection Leasing worked in XenApp 7.6](connection-leasing-how-it-works.md)
- [XenApp migration tooling: Migration Center and 6.0-to-6.5 Upgrade Utility (2013)](xenapp-migration-tooling-2013.md)
