---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, caching, resolver, performance]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DNS caching: server and client

DNS caching reduces query traffic. Two caches exist:

- **DNS server cache**: when a server performs recursive queries for clients it stores the resulting records; repeated requests are answered from cache. The cache is cleared when the DNS Server service stops, or manually via the DNS console.
- **DNS client (resolver) cache**: the per-client cache populated from query responses and the local HOSTS file.

Durable concept.

*Bron: Core Knowledge doc 'DNS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DNS conditional forwarders](dns-conditional-forwarders.md)
- [DNS recursion vs iteration and root hints](dns-recursion-vs-iteration.md)
- [DNS resource record types](dns-resource-record-types.md)
- [Host Name Resolution and Routing Process](host-routing-and-arp-process.md)
- [Windows name resolution order: DNS and NetBIOS/WINS (reference)](windows-name-resolution-order-dns-netbios.md)
