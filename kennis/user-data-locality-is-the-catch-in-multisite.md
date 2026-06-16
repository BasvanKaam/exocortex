---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vmware, horizon, multi-site, user-data, profile, design]
bron: basvankaam-blog
---

# Multi-site brokering is easy, user-data locality is the catch

In his May 2017 Cloud Pod write-up, Bas plants a 'VMW fact' warning that the architecture only solves half the problem: you still have to take care of the user data. If a user lands on a desktop in New York while their profile, home dir and company data sit in Europe, things will not feel snappy, so a replication mechanism is worth considering, and the WAN/MAN links in between are assumed to be low-latency. This is his consistent practitioner's instinct: the broker/federation layer is the glamorous part, but data gravity and latency are where real deployments hurt. A durable design caution that applies to any geo-distributed VDI, not just Horizon.

*Bron: blogpost 'VMware Cloud Pod Architecture explained' (2017-05-07), basvankaam.com.*

## Verwante notities

- [Printing and scanning are the trap when hosting RDSH/VDI in the cloud](cloud-printing-scanning-bandwidth-latency.md)
- [FSLogix Cloud Cache (tech preview, 2018)](fslogix-cloud-cache-2018.md)
- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [NetScaler GSLB is DNS-based multi-site traffic management](netscaler-gslb-dns-foundation.md)
- [GSLB selection metrics and the Metric Exchange Protocol](netscaler-gslb-metrics-mep.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [VMware Cloud Pod Architecture aggregates pods behind one entitlement layer](vmware-cloud-pod-architecture.md)
