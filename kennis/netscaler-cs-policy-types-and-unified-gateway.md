---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, content-switching, classic-policy, default-syntax, unified-gateway, gateway]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Content switching policy types and Unified Gateway

How it worked then. Three content switching policy types:
- Domain-based: matches the incoming URL's domain. Classic policies only.
- URL-based: matches the incoming URL, returning the longest matching configured URL. Classic policies only.
- Rule-based: matches incoming data against expressions; supports both classic and default-syntax policies.

Classic vs default-syntax: default-syntax policies (formerly 'Advanced policies') can evaluate more data and configure more operations; they require an assigned priority, whereas classic policies make priority optional.

HTTP-header switching: the NetScaler can redirect based on cookie, language, device type, HTTP method (GET/POST), or layer 3/4 info (source/dest IP and ports) read from the header.

Gateway binding: as of Gateway 10.5 you can bind content switching policies directly to a NetScaler Gateway vServer; the policy engine checks CS policies first, and unmatched traffic flows through the Gateway vServer as normal.

Unified Gateway (NetScaler 11): receives traffic on one external IP and directs it to load balance vServers bound to the Unified Gateway vServer, freeing up external IPs. The content switching vServer is the primary component of Unified Gateway - it's content switching under the hood, optionally fronted by a Gateway vServer handling external authentication.

*Bron: blogpost 'Citrix NetScaler… The basics continued, part six. Content Switching' (2015-11-11), basvankaam.com.*

## Verwante notities

- [NetScaler content switching: one entry point, many back ends](netscaler-content-switching-basics.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
