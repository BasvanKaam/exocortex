---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [fma, ima, xendesktop, database, local-host-cache]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Why the FMA Site database is a single point of failure (no Local Host Cache)

How it worked then (XenDesktop 7, 2013): the FlexCast Management Architecture (FMA) made the SQL Site Configuration Database critical because FMA servers, unlike the older IMA XenApp servers, had **no Local Host Cache (LHC)**.

Under IMA, each server held an LHC, a recent copy of the central database synchronized every 30 minutes by default. If the central database went unreachable, servers kept running off the LHC: new users could still connect and almost everything kept working, except admins could not make configuration changes.

Under FMA there was no such fallback, so when the database is down, users cannot connect and IT cannot make changes. That is why some form of SQL high availability was effectively mandatory. (Citrix later reintroduced an LHC for FMA in XenApp/XenDesktop 7.x, so this gap was eventually closed.)

*Bron: blogpost 'XenDesktop SQL High Availability... What to use?!' (2013-12-16), basvankaam.com.*

## Verwante notities

- [Connection Leasing is not Local Host Cache, and it's not HA](cl-is-not-lhc-and-not-ha.md)
- [On over-engineering HA: simplicity often wins, but it all depends](ha-it-all-depends.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [Losing Local Host Cache was a real FMA regression](no-local-host-cache-fma-drawback.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
