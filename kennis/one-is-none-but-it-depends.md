---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, high-availability, architecture, cost, pragmatism]
bron: basvankaam-blog
---

# "One is none, two is one" -- but HA is a policy decision, not a dogma

In July 2016 Bas pushes back on the reflex to always double up every Citrix component. He preaches redundancy himself for larger, business-critical environments, but argues there are exceptions and it all depends. For companies running light-to-medium workloads, a 30-minute outage of the central Site database (no new sessions or reconnects) might frustrate users but won't sink the business. His framing is to ask four questions: how likely is the FMA database to fail, what is the real business impact, how long to restore, and is it worth the extra Microsoft Server and SQL licenses. His closing defence of the unorthodox single-machine approach: "Just because nobody is doing it or talking about it, doesn't mean it can't be done or that it is a wrong approach."

*Bron: blogpost 'Citrix XenApp single machine setup - Cheap, fast and supported!' (2016-07-12), basvankaam.com.*

## Verwante notities

- [Azure Availability Sets vs Availability Zones](azure-availability-sets-vs-zones.md)
- [Firm believer in choice: spread options, but cap the platform count](firm-believer-in-choice-no-one-size-fits-all.md)
- [Why the FMA Site database is a single point of failure (no Local Host Cache)](fma-no-local-host-cache-db-dependency.md)
- [On over-engineering HA: simplicity often wins, but it all depends](ha-it-all-depends.md)
- [Use LHC over Connection Leasing, and the FMA's modularity proves itself](lhc-over-connection-leasing.md)
- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- [One is none: always deploy two StoreFronts and two Delivery Controllers](one-is-none-storefront-dc-redundancy.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
- [HA options for the XD7 Site configuration database](xd7-site-db-ha-options.md)
- [XenDesktop 7.6 HA options before Zones](xendesktop-76-ha-options-pre-zones.md)
