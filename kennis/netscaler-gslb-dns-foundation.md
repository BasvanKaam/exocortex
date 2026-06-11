---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, gslb, dns, adns, multi-site, disaster-recovery]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler GSLB is DNS-based multi-site traffic management

How it worked (2015), concept still relevant. GSLB (Global Server Load Balancing) manages traffic flow between two or more geographically dispersed data centres for load balancing, HA, fault tolerance or DR. The mechanism is built on DNS: a configured NetScaler acts as the authoritative (or sub-domain) nameserver for the domain(s) you want to steer across sites (it can also act as a proxy for internal authoritative nameservers).

Components:
- GSLB domain containing at least two GSLB sites (one per data centre); each NetScaler treats its own site as local and others as remote.
- A GSLB service per NetScaler, bound to a load balancing, content switching or NetScaler Gateway vServer.
- A GSLB vServer that references the GSLB services and balances between them.
- The ADNS (authoritative DNS) service that answers DNS queries and hands them to the GSLB vServer.

Licensing: GSLB required Enterprise or Platinum NetScaler licences. Important design rule: do NOT enable HA between the local and remote NetScalers in a GSLB pair - they must function independently.

*Bron: blogpost 'Citrix NetScaler… The basics continued, part five. Global Server Load Balancing' (2015-10-20), basvankaam.com.*

## Verwante notities

- [GSLB selection metrics and the Metric Exchange Protocol](netscaler-gslb-metrics-mep.md)
- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [Multi-site brokering is easy, user-data locality is the catch](user-data-locality-is-the-catch-in-multisite.md)
- [VMware Cloud Pod Architecture aggregates pods behind one entitlement layer](vmware-cloud-pod-architecture.md)
