---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, high-availability, failover, storefront]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenDesktop 7.6 HA options before Zones

How making XenDesktop 7.6 workloads highly available looked in late 2015, per a Bas van Kaam / Wilco van Bragt E2EVC session. Notably, Zones were not yet an option. The HA and failover toolkit at the time relied on: StoreFront multi-site configurations, Connection Leasing, Application Groups, and load balancing. The session also covered what was still missing from an HA perspective in their view, framing the gaps as openly as the capabilities. Useful as a marker of the pre-Zones era of Citrix HA design.

*Bron: blogpost 'E2EVC... The one in Lisbon. The XD 7.6 HA (im)possibilities - presentation video!' (2016-04-28), basvankaam.com.*

## Verwante notities

- [On over-engineering HA: simplicity often wins, but it all depends](ha-it-all-depends.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
- [One is none: always deploy two StoreFronts and two Delivery Controllers](one-is-none-storefront-dc-redundancy.md)
- [New FMA features land in Citrix Workspace Cloud first, then on-prem](positie-zones-and-cloud-first-feature-flow.md)
