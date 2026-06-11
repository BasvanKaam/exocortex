---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [sta, netscaler, broker-service, security]
layer: reference
bron: inside-citrix-fma
---

# The Secure Ticket Authority (STA)

The Secure Ticket Authority (STA) was first introduced with an early Secure Gateway edition over twelve years ago. It runs as a service and is part of the Broker Service on the Delivery Controller (like the XML service). During a resource launch, both the StoreFront server and the NetScaler must communicate with the STA, so NetScaler and StoreFront/Web Interface must point to the exact same XML/STA service(s)/Delivery Controller(s).

The NetScaler Gateway uses the STA to guarantee each user is successfully authenticated: a valid STA ticket means the user passed the web-server authentication checks and may be granted access. It prevents outside computers from knowing about the inside network and authorises the NetScaler Gateway ICA Proxy to set up a connection from outside to inside, specifying where an outbound connection may connect on the inside.

When a resource is launched through NetScaler Gateway, an STA ticket is requested and ends up in the launch.ica file. The Delivery Controller hosting the STA holds the ticket in memory for a configurable time. The STA is only used when traffic traverses a NetScaler, so internal StoreFront authentication does not involve STA tickets.

## Verwante notities

- [Broker Service: XML, STA and the Principal Broker](broker-service-xml-sta-principal.md)
- [The STA only comes into play when traffic traverses a NetScaler](citrix-sta-only-with-netscaler.md)
- [CWC authentication and credential handling security](cwc-authentication-credential-handling.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [External launch process: Hosted Shared Desktop via NetScaler](external-launch-process-hsd-netscaler.md)
- [FMA Broker Service (XML/STA) and its responsibilities](fma-broker-service.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [NetScaler SNIP, STA tickets and certificate practice](netscaler-snip-and-sta.md)
- [Optimal NetScaler Gateway routing](optimal-netscaler-gateway-routing.md)
