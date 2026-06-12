---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, netscaler, split-tunneling, ssl-vpn, gateway, intranet-applications, networking]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler split tunneling: route only corporate traffic through the VPN

How it worked then: split tunneling is an SSL VPN feature controlling what traffic the client (NetScaler Gateway Plugin) sends through the VPN tunnel versus directly onto its local network/Internet. Two options when a remote user connects (e.g. from a cafe): (1) send all traffic through the NetScaler Gateway, including Internet-bound traffic, so you can control and inspect everything, at the cost of extra load on the NetScaler; or (2) split tunneling, where only traffic destined for the corporate network goes through the Gateway over the SSL VPN and all other traffic goes straight to the Internet from the user's device. With split tunneling, the plugin (Windows transparent / Java proxy mode) gets a list of configured Intranet Applications on startup and inspects destination addresses in each packet; matches go through the Gateway, non-matches are sent directly to the Internet. The point: prevent the plugin from sending unnecessary (non-corporate) traffic through the Gateway. NetScaler also supports reverse split tunneling, where traffic to the configured internal addresses is NOT routed through the Gateway.

*Bron: blogpost 'Citrix NetScaler… The basics continued, part seven. Split Tunneling!' (2016-03-13), basvankaam.com.*

## Verwante notities

- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [Intranet Applications: the subnet objects that define split tunneling](netscaler-intranet-applications-object.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [NetScaler SNIP, MIP and static routes: how traffic is sourced and routed](netscaler-snip-mip-static-routes.md)
- [Office 365 Network Performance: Service Front Doors and the Basics](office365-network-performance-basics.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
