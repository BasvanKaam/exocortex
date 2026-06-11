---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dhcp, relay-agent, bootp, routing, rras]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DHCP relay agent across subnets

Because DHCPDISCOVER is a broadcast and broadcasts do not cross routers unless explicitly forwarded, a routed network with a single DHCP server needs a DHCP relay agent (or a router configured to forward DHCP/BOOTP) so discover messages reach the server. For multi-segment networks the options are: a DHCP server per segment, a relay agent per segment, or routers configured to forward the broadcasts.

To hand DHCP-obtained addresses to remote access clients, an RRAS server is configured to allocate addresses via DHCP and uses a relay agent on the remote access server or its subnet.

The relay concept is durable; the RRAS specifics are Windows-flavored but the principle holds.

*Bron: Core Knowledge doc 'DHCP Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DHCP 80/20 redundancy rule](dhcp-80-20-rule.md)
- [DHCP DORA lease process](dhcp-dora-lease-process.md)
- [DHCP lease renewal timers](dhcp-lease-renewal-timers.md)
- [DHCP security threats](dhcp-security-threats.md)
- [DNS and DHCP Command-Line Tools](dns-dhcp-cli-tools.md)
- [Host Name Resolution and Routing Process](host-routing-and-arp-process.md)
- [ISA Server 2004/2006 Configuration Concepts](isa-server-configuration-concepts.md)
- [Subnetting and VLANs](subnetting-and-vlans.md)
