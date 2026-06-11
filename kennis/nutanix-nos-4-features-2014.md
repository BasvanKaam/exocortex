---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [nutanix, nos, prism, data-protection, dated-2014]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How Nutanix NOS 4.0 worked: Prism Central, integrated data protection, one-click upgrade

How it worked then (April 2014, NOS 4.0):

- Prism Central: the HTML5 management framework, renamed from Prism because 4.0 added true multi-cluster management. It let you manage many clusters across locations from a single pane of glass, with SSO across clusters and aggregated health/usage data including historical data.
- Integrated data protection: built into Prism, it scheduled and managed local and remote snapshots for backup and DR, with WAN-optimized replication for multi-site/DR scenarios. Compatible with both ESXi and Hyper-V; could replicate to off-cluster storage (e.g. via Veeam). One-click restore.
- One-click NOS upgrade: nodes upgraded in parallel, reboots sequenced in serial, transparent to users (Nutanix compared it to upgrading an iOS device).
- Cluster Health: a background service monitoring VMs, nodes and disks across all clusters managed through Prism Central, surfacing warnings, failures and critical alerts.
- MapReduce deduplication: NOS 3.5's elastic dedup engine was complemented with MapReduce dedup, distributing dedup work across all cluster nodes for true scale-out, global deduplication.

Dated specifics, kept as a snapshot of where hyperconverged management tooling was in 2014.

*Bron: blogpost 'Introducing Nutanix OS (NOS) 4.0... What's new?!' (2014-04-15), basvankaam.com.*

## Verwante notities

- [Dell XC series: same Nutanix software, different hardware](dell-xc-nutanix-oem-model.md)
- [Nutanix Acropolis is three components, not just a hypervisor](nutanix-acropolis-three-components.md)
