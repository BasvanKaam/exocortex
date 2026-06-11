---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [fma, ima, zones, local-host-cache, storefront, architecture]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FMA dropped zones and Local Host Cache

How it worked then: with the Flex Management Architecture (XenDesktop 7) zones disappeared along with the Local Host Cache (LHC) that IMA/XenApp had. Consequences:

- The central SQL database became critical: if it's down the Site accepts no new connections (no LHC fallback) and you can't make config changes. Bas notes SQL clustering/mirroring helps but 'often it doesn't' hold up.
- To get the zone-like behaviour (geographic load balancing, point users near their data, recovery sites) you now create separate Sites and stitch them together with StoreFront Multi-Site configurations, no NetScaler strictly required.
- WebInterface is replaced by StoreFront. XenApp admins moving to FMA must rethink designs around FMA vs IMA.

*Bron: blogpost 'Configure StoreFront Multi-Site configurations' (2013-12-02), basvankaam.com.*

## Verwante notities

- [Critique: why isn't this in the GUI? (web.config friction)](build-it-into-the-gui-position.md)
- [FMA vs IMA: no Zones, no Data Collectors, no Local Host Cache (2013)](fma-vs-ima-no-zones-no-lhc.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
