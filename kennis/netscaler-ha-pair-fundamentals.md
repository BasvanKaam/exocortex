---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, high-availability, failover, replication, citrix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler HA pair: heartbeats, failover and config replication

How NetScaler High Availability worked around 2015.

- An HA pair is 2 to a max of 64 NetScaler appliances (VPX included). One node is primary/active; the others are secondary/passive.
- Secondary nodes send a continuous stream of heartbeat messages (configurable interval) to check the primary. If the primary fails to respond after multiple retries, a secondary takes over (failover).
- The primary handles all incoming traffic for the configured virtual servers, VIPs, SNIPs, MIPs and enabled features.

Pairing requirements:
- Both NetScalers must be the same model and make (different models can't be paired).
- Same software version and licenses.
- The ns.conf files must be identical except for the NSIP addresses and the id/IP of the other HA node.

Management and replication:
- Each node has its own NSIP, but all management and config must be done on the primary only. Enabling management on a Subnet IP always routes you to the current primary.
- Changes on the primary auto-replicate (enabled by default) to the secondary, one-way: SNIPs/routes, interfaces, MIPs, VIPs, static routes, policies, monitors, everything.
- Sync can also be triggered manually and is auto-triggered when a secondary reboots or when a former primary becomes secondary after failover. Caution: forcing sync from the secondary overwrites the primary's config.
- After failover clients reconnect, but session persistence rules are maintained. Failover can be triggered manually for testing/maintenance.

Always back up the current config before major changes, and take precautions when adding a second node so the primary's config isn't accidentally overwritten.

*Bron: blogpost 'Citrix NetScaler basics part three: High Availability' (2015-09-02), basvankaam.com.*

## Verwante notities

- [NetScaler GSLB is DNS-based multi-site traffic management](netscaler-gslb-dns-foundation.md)
- [GSLB selection metrics and the Metric Exchange Protocol](netscaler-gslb-metrics-mep.md)
- [NetScaler high availability and clustering](netscaler-high-availability-clustering.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [NetScaler monitors: why load balancing needs health checks](netscaler-monitors-health-checking.md)
- [NetScaler platforms, editions and HA](netscaler-platforms-and-licensing.md)
- [NetScaler 10.1 TFTP load balancing for PVS boot HA](netscaler-tftp-load-balancing-pvs.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
- [One is none: always deploy two StoreFronts and two Delivery Controllers](one-is-none-storefront-dc-redundancy.md)
