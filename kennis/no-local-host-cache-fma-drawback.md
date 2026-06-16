---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, local-host-cache, ima, database, positie]
bron: basvankaam-blog
---

# Losing Local Host Cache was a real FMA regression

In the comments on this post (late 2014), Bas flags a genuine drawback of early FMA versus the older IMA architecture: when the central Site database is down or unreachable, there is no load balancing taking place. He names this explicitly as 'one of the drawbacks when compared to LHC' (Local Host Cache), which XenApp 6.5 and earlier had under IMA. Context: Citrix later reintroduced LHC to the FMA, so this captures the moment when its absence was a recognized weakness. Also notable: he repeatedly mentions he is 'working on a book project' that will cover this material, showing the cheat sheet as the on-ramp to his book.

*Bron: blogpost 'The ultimate Citrix XenDesktop 7.x internals cheat sheet!' (2014-11-24), basvankaam.com.*

## Verwante notities

- [Connection Leasing is not Local Host Cache, and it's not HA](cl-is-not-lhc-and-not-ha.md)
- [How Connection Leasing worked in XenApp 7.6](connection-leasing-how-it-works.md)
- [Why the FMA Site database is a single point of failure (no Local Host Cache)](fma-no-local-host-cache-db-dependency.md)
- [FMA Site database vs IMA store and the missing LHC](fma-site-db-vs-ima-store-lhc.md)
- [FMA vs IMA: no Zones, no Data Collectors, no Local Host Cache (2013)](fma-vs-ima-no-zones-no-lhc.md)
- [Use LHC over Connection Leasing, and the FMA's modularity proves itself](lhc-over-connection-leasing.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [Writing the FMA book was brutal but never regretted](self-publishing-fma-book-worth-it.md)
- [VDA high-availability mode for Controller outages](xd7-vda-high-availability-mode.md)
