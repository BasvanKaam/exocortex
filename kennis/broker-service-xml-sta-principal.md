---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [broker-service, xml-service, sta, lhc, principal-broker]
layer: reference
bron: inside-citrix-fma
---

# Broker Service: XML, STA and the Principal Broker

The Broker Service is built from three services handling different tasks: it brokers connections, enumerates resources, and acts as the Secure Ticket Authority (generating/validating STA tickets).

The STA service has been part of the Broker service since Presentation Server 4.0; before that it was an ISAPI extension for Microsoft IIS. The XML service (ctxxmlss.exe) was rewritten in .NET and became part of the Broker service as of XenDesktop 4.x.

With the reintroduction of the Local Host Cache (LHC), the Broker service is also known as the Principal Broker Service. Every two minutes the (Principal) Broker Service is checked for configuration changes; if a change is detected it is copied/synchronised to the High Availability Service / Secondary Broker Service.

FMA fact: make sure the Broker (XML/STA) service is configured identically on the NetScaler and the StoreFront server, including the load-balance/fail-over order.

## Verwante notities

- [Bas's distinction: authentication versus verification](authentication-vs-verification-distinction.md)
- [Bas's key takeaways on the user login process](bas-key-takeaways-user-login-process.md)
- [The STA only comes into play when traffic traverses a NetScaler](citrix-sta-only-with-netscaler.md)
- [External launch process: Hosted Shared Desktop via NetScaler](external-launch-process-hsd-netscaler.md)
- [FMA Broker Service (XML/STA) and its responsibilities](fma-broker-service.md)
- [NetScaler SNIP, STA tickets and certificate practice](netscaler-snip-and-sta.md)
- [The Secure Ticket Authority (STA)](secure-ticket-authority-sta.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
- [StoreFront vs Web Interface user authentication](storefront-vs-web-interface-authentication.md)
