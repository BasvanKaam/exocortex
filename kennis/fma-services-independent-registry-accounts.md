---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, architecture, registry, high-availability]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FMA services run independently, with separate DB connection strings

How it worked then: all FMA services run completely independent of each other - if one goes offline it doesn't directly affect the others. Each service points to the central Site database but has an independent registry location, so their DB connection strings are stored separately, eliminating a single point of failure.

All FMA services run under the NT AUTHORITY\Network service account, and when authenticating to the central Site database they use the local computer account of the machine they run on. Delivery Controller check-in detail: a Controller registers with the central Site DB every 20 seconds (valid for another 40 seconds); the 'last registered' minutes value shown per Controller in Studio should always be 0.

*Bron: blogpost '12 services that make up the Citrix XenDesktop Flex Management Architecture' (2015-03-26), basvankaam.com.*

## Verwante notities

- [Check FMA service health with PowerShell, not just Director](check-fma-services-with-powershell.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [FMA architecture: Controllers, Agents and a critical central database (durable)](fma-controllers-agents-central-database.md)
- [The FMA core services and how they communicate](fma-services-complete-overview.md)
- [FMA service high availability via peer service groups](fma-services-high-availability.md)
- [FMA services: Network Service account and service isolation](fma-services-network-account-and-isolation.md)
- [The FMA's 10 (or 12) primary services and their roles](fma-twelve-services-rundown.md)
