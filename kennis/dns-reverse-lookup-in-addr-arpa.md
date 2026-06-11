---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, reverse-lookup, in-addr-arpa, ptr]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DNS reverse lookup and in-addr.arpa

A forward lookup finds an IP from a name (via an A record). A **reverse lookup** finds a name from a known IP. DNS was not originally designed for this, because the namespace indexes names while IPs are assigned differently, so a naive reverse search would be impractical.

The solution is the special **in-addr.arpa** domain. Reverse subdomains are formed from the IP octets in reversed order, because IP addresses read left-to-right go from most general (network) to most specific (host), the opposite of DNS names. A reverse query for 192.168.1.20 becomes the FQDN 20.1.168.192.in-addr.arpa, which a **PTR** record answers with the host's DNS name. If the reverse name is not locally answerable, normal recursion or iteration locates the authoritative reverse-lookup zone.

Durable DNS fundamental.

*Bron: Core Knowledge doc 'DNS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DNS recursion vs iteration and root hints](dns-recursion-vs-iteration.md)
- [DNS resource record types](dns-resource-record-types.md)
- [DNS zone types](dns-zone-types.md)
- [Host Name Resolution and Routing Process](host-routing-and-arp-process.md)
- [Windows name resolution order: DNS and NetBIOS/WINS (reference)](windows-name-resolution-order-dns-netbios.md)
