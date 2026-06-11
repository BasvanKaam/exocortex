---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, recursion, iteration, root-hints, name-resolution]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DNS recursion vs iteration and root hints

**Recursion**: the preferred resolution method, where the DNS server itself queries other DNS servers on the client's behalf, effectively becoming a DNS client. Some admins disable recursion for performance, forcing iteration instead.

**Iteration**: the server answers a query either with the result or with a referral to another server that is closer to the answer; the original client must then re-query the referred server, repeating until the authoritative server is found.

**Root hints**: when a server does not know an address it forwards toward a server it does know. Root hints are a preconfigured list of the authoritative root-level DNS servers (name plus IP). On Windows Server they lived in CACHE.DNS under \Windows\System32\Dns. The root servers hold the Root Zone File, which lists the authoritative servers for each Top Level Domain (.com, .edu, etc.), maintained largely by IANA.

These mechanics are durable DNS concepts.

*Bron: Core Knowledge doc 'DNS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DNS caching: server and client](dns-caching-server-and-client.md)
- [DNS conditional forwarders](dns-conditional-forwarders.md)
- [DNS resource record types](dns-resource-record-types.md)
- [DNS reverse lookup and in-addr.arpa](dns-reverse-lookup-in-addr-arpa.md)
- [DNS zone transfer and Notify](dns-zone-transfer-and-notify.md)
- [DNS zone types](dns-zone-types.md)
- [Host Name Resolution and Routing Process](host-routing-and-arp-process.md)
- [Windows name resolution order: DNS and NetBIOS/WINS (reference)](windows-name-resolution-order-dns-netbios.md)
