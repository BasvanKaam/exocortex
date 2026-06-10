---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, static-route, networking]
layer: reference
bron: inside-citrix-fma
---

# NetScaler static routes

SNIP addresses only work with directly reachable subnets. To reach a subnet that isn't directly connected, you configure a **static route**.

Example: you have a SNIP connecting the NetScaler to subnet A, but you also need subnet D, which is only reachable through subnet A via a routing device. Adding another SNIP for subnet D won't work because D isn't directly reachable. Instead you add a static route telling the NetScaler to route traffic destined for subnet D over/through subnet A, including the IP address of the routing device connected to subnet D. If no known route to D is configured, the NetScaler forwards all such traffic to its default route.

## Verwante notities

- [NetScaler IP addresses: NSIP, SNIP and MIP](netscaler-ip-addresses-nsip-snip-mip.md)
- [NetScaler SNIP, STA tickets and certificate practice](netscaler-snip-and-sta.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [NetScaler vServers, service objects and server objects](netscaler-virtual-server-service-server-objects.md)
