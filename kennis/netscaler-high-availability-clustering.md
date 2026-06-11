---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, high-availability, clustering, failover]
layer: reference
bron: inside-citrix-fma
---

# NetScaler high availability and clustering

NetScaler **HA (2 nodes)** is always **active-passive**: one node is primary (active), the secondary sends a continuous stream of heartbeat messages (configurable interval) to check whether the primary is active and accepting connections. If the primary fails to respond after multiple retries, the secondary takes over — a **failover**.

NetScaler **clustering** is **active/active using ECMP** and can grow up to **32 nodes**.

Important constraint: when applying HA, different NetScaler models cannot be paired — both appliances must be the same make and model and run the same software version, licenses included. Bas invokes the 'one is none' rule: NetScalers should be made redundant too.

The NetScaler can also provide secure remote access to XenMobile web, SaaS and mobile applications; mobile app access is via **Micro VPNs**, for which a NetScaler is required. It can secure remote access for both StoreFront and the older Web Interface. Implementing a NetScaler requires opening certain firewall ports — always check the Citrix product documentation first.

## Verwante notities

- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
- [NetScaler appliance models: VPX, MPX, SDX, CPX](netscaler-appliance-models-vpx-mpx-sdx-cpx.md)
- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- [NetScaler platforms, editions and HA](netscaler-platforms-and-licensing.md)
- [NetScaler vServers, service objects and server objects](netscaler-virtual-server-service-server-objects.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
- [StoreFront high availability and Delivery Controller load balancing](storefront-ha-and-load-balancing.md)
