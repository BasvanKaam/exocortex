---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, netbios, wins, hosts, lmhosts, name-resolution, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Windows name resolution order: DNS and NetBIOS/WINS (reference)

Two name types had to be resolved: **DNS host names** (used by winsock/sockets apps like ping and telnet) and **NetBIOS names** (used by most classic Microsoft network functions such as browsing and mapping drives).

DNS resolution order: local DNS client cache, then the local HOSTS file, then a DNS server query.

NetBIOS resolution order (WINS): NetBIOS name cache, primary WINS server, secondary WINS server, broadcast, then the LMHOSTS file. Mnemonic from the notes: HOSTS is the DNS-name alternative to a DNS server; LMHOSTS is the NetBIOS-name alternative to a WINS server.

**WINS** maintained a database of NetBIOS-name-to-IP mappings; clients configured to use a WINS server as NetBIOS name server (NBNS) were WINS clients, others were broadcast clients. If a DNS server did not respond, it was retried at 1, 2, 2, and 4 second intervals before falling back.

The HOSTS/DNS resolution path and the in-cache/ARP/broadcast hardware-address steps are durable; the NetBIOS/WINS/LMHOSTS layer is dated legacy infrastructure, hence reference.

*Bron: Core Knowledge doc 'DNS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DNS caching: server and client](dns-caching-server-and-client.md)
- [DNS conditional forwarders](dns-conditional-forwarders.md)
- [DNS and DHCP Command-Line Tools](dns-dhcp-cli-tools.md)
- [DNS recursion vs iteration and root hints](dns-recursion-vs-iteration.md)
- [DNS resource record types](dns-resource-record-types.md)
- [DNS reverse lookup and in-addr.arpa](dns-reverse-lookup-in-addr-arpa.md)
- [Host Name Resolution and Routing Process](host-routing-and-arp-process.md)
