---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [networking, routing, arp, dns, reference]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Host Name Resolution and Routing Process

The end-to-end sequence when a host sends data to a named destination:

1. The name is first resolved to an IP address via the DNS server.
2. The host checks its local routing table to see whether the address is reachable.
3. If the destination is on the local network, the host checks its ARP cache for the matching MAC address.
4. If the MAC is not cached, the host sends an ARP broadcast, waits for the reply, and adds the returned MAC address to the ARP cache.
5. The data is sent to that MAC address.
6. If no local route is found in the routing table, the data is sent to the default gateway.
7. The gateway (usually a router) checks its own routing table for a route to the destination. If it finds one, it replies with its own MAC address and the workstation sends the data to the router's MAC.
8. If the gateway has no route, it forwards to the next gateway and the process repeats.

These fundamentals (DNS → routing table → ARP → default gateway hop-by-hop) remain true today.

*Bron: Core Knowledge doc 'Algemene Routering Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Classful IP addressing (historical reference)](classful-ip-addressing.md)
- [DHCP relay agent across subnets](dhcp-relay-agent.md)
- [DNS caching: server and client](dns-caching-server-and-client.md)
- [DNS recursion vs iteration and root hints](dns-recursion-vs-iteration.md)
- [DNS reverse lookup and in-addr.arpa](dns-reverse-lookup-in-addr-arpa.md)
- [RFC 1918 private IP address ranges](rfc1918-private-ip-ranges.md)
- [Subnetting and VLANs](subnetting-and-vlans.md)
- [Windows name resolution order: DNS and NetBIOS/WINS (reference)](windows-name-resolution-order-dns-netbios.md)
