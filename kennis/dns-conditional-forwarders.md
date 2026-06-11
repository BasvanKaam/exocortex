---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, forwarders, conditional-forwarder, name-resolution]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DNS conditional forwarders

A conditional forwarder resolves names only for a specific domain. For example, you can configure a server to send any request for hosts in google.com directly to a name server authoritative for google.com. This speeds resolution by skipping the trip up to the root to find that authoritative server.

Durable concept.

*Bron: Core Knowledge doc 'DNS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DNS caching: server and client](dns-caching-server-and-client.md)
- [DNS recursion vs iteration and root hints](dns-recursion-vs-iteration.md)
- [DNS resource record types](dns-resource-record-types.md)
- [DNS zone types](dns-zone-types.md)
- [Windows name resolution order: DNS and NetBIOS/WINS (reference)](windows-name-resolution-order-dns-netbios.md)
