---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, zone-transfer, ixfr, axfr, dns-notify, replication]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DNS zone transfer and Notify

A zone transfer copies resource records from the primary to secondary DNS servers so a secondary can keep answering if the primary fails.

- **Full transfer (AXFR)**: a newly started secondary requests a complete copy of the zone; resource-intensive.
- **Incremental transfer (IXFR)**: only records changed since the last transfer are sent. The databases are compared by serial number; if the primary's serial is higher than the secondary's, only the delta records transfer. Requires the primary to record incremental changes; uses less bandwidth.
- **Active Directory transfers**: occur when AD-integrated zones replicate to domain controllers, via AD replication rather than DNS transfer.

**DNS Notify**: lets a primary tell secondaries that its database changed so they initiate a transfer (incremental or full) promptly, rather than waiting on the refresh interval.

Durable DNS concepts.

*Bron: Core Knowledge doc 'DNS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [DNS recursion vs iteration and root hints](dns-recursion-vs-iteration.md)
- [DNS resource record types](dns-resource-record-types.md)
- [DNS zone types](dns-zone-types.md)
- [Synchronous vs Asynchronous Replication](synchronous-vs-asynchronous-replication.md)
