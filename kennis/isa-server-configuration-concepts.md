---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [isa-server, firewall, vpn, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# ISA Server 2004/2006 Configuration Concepts

How Microsoft's ISA Server firewall/proxy (2004/2006, now discontinued) was structured:

- **Networks**: define all networks including IP ranges, plus network objects such as VPN clients.
- **Virtual Private Networks**: VPN locations/networks (e.g. a site-to-site VPN) are defined separately here.
- **Network Rules**: which networks may communicate with each other, and whether via Route or NAT.
- **Firewall Policy**: what is allowed inbound and outbound — from outside to which internal network, between internal networks, and from internal networks outbound — specifying protocols and port numbers. Requires the network rules to be correctly defined first.
- **Server Publishing**: makes an internal server reachable from outside. A public name (e.g. host.example.com) arrives on a listener (an IP on ISA's external NIC, which has several IPs) and is routed to an internal site name or IP. Link translation rewrites links in published web content that reference internal server names into the public name.
- **System Policy**: where ISA itself is configured (e.g. RDP settings).

*Bron: Core Knowledge doc 'ISA Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DHCP relay agent across subnets](dhcp-relay-agent.md)
- [Innovation Comes From Outside the Firewall](innovation-comes-from-outside-the-firewall.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [Subnetting and VLANs](subnetting-and-vlans.md)
