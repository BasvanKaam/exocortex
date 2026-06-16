---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, content-switching, vserver, load-balancing, policy, http-header]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler content switching: one entry point, many back ends

How it worked (2015), concept still current. Content switching gives a single point of entry (one IP, potentially multiple domains/URLs) that routes incoming traffic to various back-end services (XenApp, XenDesktop, web portals, webmail, ShareFile, mobile platforms, etc.). Each service type gets a content switching policy bound to the content switching vServer; the matching policy forwards the request to a corresponding load balance vServer.

Build order (steps 1-4 form a 'Content Group'):
1. Enable the content switching feature.
2. Create a content switching vServer with a VIP.
3. Create at least two load balance vServers to forward to (these don't need their own VIP when used behind content switching).
4. Create at least two content switching policies (one per service/content type) and bind them to the CS vServer.
5. Create the services, server objects and monitors and bind them.

Flow: request hits the CS vServer to policies evaluated in priority/creation order to first match wins to traffic forwarded to the bound load balance vServer. Licensing: needs a NetScaler Standard licence or higher; a NetScaler Gateway licence alone is not sufficient. A CS vServer can only send requests to other vServers (front an external load balancer via a load balance vServer).

*Bron: blogpost 'Citrix NetScaler… The basics continued, part six. Content Switching' (2015-11-11), basvankaam.com.*

## Verwante notities

- [Content switching policy types and Unified Gateway](netscaler-cs-policy-types-and-unified-gateway.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [NetScaler monitors: why load balancing needs health checks](netscaler-monitors-health-checking.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
