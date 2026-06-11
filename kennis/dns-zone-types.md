---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, zones, stub-zone, active-directory, ad-integrated]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DNS zone types

- **Primary**: owns its zones and can change them.
- **Secondary**: holds a read-only copy obtained via zone transfer; can answer queries but cannot change data. A secondary can in turn act as master to other secondaries below it.
- **Stub zone**: a copy containing only the records needed to identify the authoritative DNS servers for a zone (SOA, NS, and glue A records, plus the master server IPs). Used to resolve names between separate namespaces, e.g. after a corporate merger. A server hosting a stub zone sends iterative queries to the authoritative servers in the stub's NS records, falling back to root hints if it cannot find them.
- **Active Directory-integrated zone**: stores zone data in AD instead of zone files; an authoritative primary zone that benefits from AD multi-master replication and AD security. Advantages over a standard primary: faster AD-driven replication (no separate DNS replication), AD security features, unified management of domains and DNS namespace, and automatic replication of zones to new domain controllers.

The AD-integration specifics are Windows-flavored but the zone-type concepts are durable.

*Bron: Core Knowledge doc 'DNS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [AD Sites and Replication Topology](ad-sites-and-replication-topology.md)
- [DNS conditional forwarders](dns-conditional-forwarders.md)
- [DNS recursion vs iteration and root hints](dns-recursion-vs-iteration.md)
- [DNS resource record types](dns-resource-record-types.md)
- [DNS reverse lookup and in-addr.arpa](dns-reverse-lookup-in-addr-arpa.md)
- [DNS zone transfer and Notify](dns-zone-transfer-and-notify.md)
