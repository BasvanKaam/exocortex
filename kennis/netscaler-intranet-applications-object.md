---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, netscaler, intranet-applications, subnet, split-tunneling, gateway-resource]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Intranet Applications: the subnet objects that define split tunneling

How it worked then: split tunneling is driven by Intranet (not Internet) Applications configured on the NetScaler as a Gateway resource. An Intranet Application is just a logical object representing a subnet (IP address + subnet mask) or range of subnets on the corporate network, a reference. When split tunneling is enabled, the addresses matched against packets from the user device refer to these Intranet Application subnets. Configuration: NetScaler Gateway > Resources > Intranet Applications > Add; give it a name, choose interception mode (transparent for Windows, proxy for the Java plugin), select destination type (IP address and netmask), protocol, and the IP/subnet or range. Then enable split tunneling globally (NetScaler Gateway > Global Settings > Client Experience tab > Split Tunneling = On) and attach the Intranet Applications.

*Bron: blogpost 'Citrix NetScaler… The basics continued, part seven. Split Tunneling!' (2016-03-13), basvankaam.com.*

## Verwante notities

- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [NetScaler SNIP, MIP and static routes: how traffic is sourced and routed](netscaler-snip-mip-static-routes.md)
- [NetScaler split tunneling: route only corporate traffic through the VPN](netscaler-split-tunneling-concept.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
