---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, sites, wan, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# AD Sites and Replication Topology

Sites limit replication and logon traffic over the WAN. A site is essentially a LAN (or several LANs joined by fast links) defined by one or more IP subnets; between sites sit slow or expensive lines. A client logging in always looks for a DC in its own site, keeping authentication and group policy delivery local and the WAN links free.

DCs within a site replicate among themselves. For replication to another site, a single DC (the bridgehead server) is responsible, so cross-site information traverses the WAN only once, unlike the BDC model in Windows NT 4.0. DFS clients also use sites: a DFS client looks for a replica in its own or a neighboring site.

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD FSMO Roles](ad-fsmo-roles.md)
- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [Domain Controller Health-Check CLI Routine](dc-health-check-cli-routine.md)
- [DFS Client Referral Process](dfs-client-referral-process.md)
- [DFS: Stand-alone vs Domain-based Namespaces](dfs-standalone-vs-domain-based.md)
- [DNS zone types](dns-zone-types.md)
- [Geographically Dispersed Clusters](geographically-dispersed-clusters.md)
