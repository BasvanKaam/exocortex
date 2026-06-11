---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [connection-leasing, local-host-cache, fma, ima, opinion]
bron: basvankaam-blog
---

# Connection Leasing is not Local Host Cache, and it's not HA

Bas's emphatic position (Oct 2014): Connection Leasing is a great addition that helped make 7.6 the best FMA-era XenApp release, "but it's no LHC." Two corrections he pushes hard:

1. CL is not a replacement for the Local Host Cache. LHC (IMA) let a server keep working, log users on/off, and even reboot with the IMA store down, indefinitely, and it sped up application enumeration. CL does none of that; an app you use only every few weeks simply won't launch if the DB is down.
2. CL is not a high-availability feature. "I've seen multiple statements that refer to Connection Leasing as a HA feature, but that's just wrong … no HA, period." He approvingly cites the Citrix E-Docs wording: CL "supplements" SQL HA best practices.

This is Bas correcting community/marketing over-claims with precision, a recurring move: respect the product, refuse the hype, insist on accurate framing.

*Bron: blogpost 'Connection Leasing vs. Local Host Cache. Conclusion? CL doesn't stand a chance!' (2014-10-06), basvankaam.com.*

## Verwante notities

- [Citrix IMA Architecture: Data Store and Local Host Cache](citrix-ima-architecture.md)
- [Connection Leasing failover behavior and limitations](connection-leasing-failover-behavior.md)
- [How Connection Leasing worked in XenApp 7.6](connection-leasing-how-it-works.md)
- [Why the FMA Site database is a single point of failure (no Local Host Cache)](fma-no-local-host-cache-db-dependency.md)
- [Use LHC over Connection Leasing, and the FMA's modularity proves itself](lhc-over-connection-leasing.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [Local Host Cache in XenApp 6.5 (IMA)](local-host-cache-ima.md)
- [Losing Local Host Cache was a real FMA regression](no-local-host-cache-fma-drawback.md)
