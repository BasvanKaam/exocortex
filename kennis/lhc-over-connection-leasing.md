---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, local-host-cache, connection-leasing, fma, opinion]
bron: basvankaam-blog
---

# Use LHC over Connection Leasing, and the FMA's modularity proves itself

December 2016. Two positions:

1. He relays and endorses Citrix's guidance: once on 7.12, use LHC over Connection Leasing, which is considered far more superior. He notes uncertainty about CL's future ('I'm not sure what the word is on CL going forward, if it will be deprecated, when etc.?').

2. He frames the rebuilt LHC as proof of the FMA's design philosophy: 'To me this again is an excellent example of the FMA's modularity and flexibility.' By recoding a couple of existing services and adding a few new ones, Citrix rebuilt LHC from the ground up rather than touching the whole package as they would have had to in the IMA-based 6.5 world, 'and for the better I'd might add.' This is a recurring through-line in his writing: the FMA's modular architecture is a genuine advantage.

*Bron: blogpost 'Local Host Cache returns in XenApp/XenDesktop 7.12, rebuilt for the FMA' (2016-12-05), basvankaam.com.*

## Verwante notities

- [Connection Leasing is not Local Host Cache, and it's not HA](cl-is-not-lhc-and-not-ha.md)
- [How Connection Leasing worked in XenApp 7.6](connection-leasing-how-it-works.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [Losing Local Host Cache was a real FMA regression](no-local-host-cache-fma-drawback.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
- [New FMA features land in Citrix Workspace Cloud first, then on-prem](positie-zones-and-cloud-first-feature-flow.md)
