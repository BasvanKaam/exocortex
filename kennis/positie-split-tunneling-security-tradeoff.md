---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, netscaler, split-tunneling, security, opinion, ssl-vpn]
bron: basvankaam-blog
---

# Split tunneling's convenience carries a real, not far-fetched, security risk

In March 2016, Bas frames the split-tunneling trade-off honestly. Full-tunnel (all traffic through the Gateway) lets you control and inspect everything and makes data harder to grab from outside, at the cost of extra NetScaler load. Split tunneling offloads the NetScaler but opens a security hole: if the remote user's computer is compromised while it still holds an active SSL VPN connection, the attacker gets full access to the corporate network too. His stance: 'while this may seem a bit far-fetched, it's still something to consider and not to be taken lightly.' A measured, security-aware consultant view rather than a blanket recommendation either way.

*Bron: blogpost 'Citrix NetScaler… The basics continued, part seven. Split Tunneling!' (2016-03-13), basvankaam.com.*

## Verwante notities

- [If traffic is inspected and users authenticated, the DMZ is at least as safe as the LAN](dmz-not-automatically-safer-than-lan.md)
- [A framework for deciding DMZ vs internal LAN server placement](dmz-placement-decision-framework.md)
- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [Intranet Applications: the subnet objects that define split tunneling](netscaler-intranet-applications-object.md)
- [NetScaler split tunneling: route only corporate traffic through the VPN](netscaler-split-tunneling-concept.md)
- [Teaching stance: master the basics before the advanced NetScaler features](netscaler-walk-before-you-run-teaching.md)
- [Optimal NetScaler Gateway routing](optimal-netscaler-gateway-routing.md)
- [SSL handshake: asymmetric to exchange, symmetric to transfer](ssl-handshake-symmetric-asymmetric.md)
