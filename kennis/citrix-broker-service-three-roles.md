---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, broker, xml-service, sta, local-host-cache, delivery-controller]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The Broker Service bundles brokering, XML and STA in one process

In the FMA architecture the Broker Service on the Delivery Controller is actually several services in one, all handling different tasks: it brokers connections, enumerates resources, maintains the Local Host Cache (LHC), and acts as the Secure Ticket Authority generating and validating STA tickets.

History worth keeping: the STA became part of the Broker Service as of Presentation Server 4.0 (before that it was an ISAPI extension for IIS). The XML service (ctxxmlss.exe) was rewritten in .NET and folded into the Broker Service as of XenDesktop 4.x. A newer Principal Broker Service can be counted as a fourth component. How it worked then, but the architectural point (one process wearing several hats) explains a lot of troubleshooting behaviour.

*Bron: blogpost 'Demystifying the Citrix XenApp logon, enumeration and launch steps' (2016-12-19), basvankaam.com.*

## Verwante notities

- [The STA only comes into play when traffic traverses a NetScaler](citrix-sta-only-with-netscaler.md)
- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [How Connection Leasing worked in XenApp 7.6](connection-leasing-how-it-works.md)
- [The eighteen Broker Service Site services (distributed housekeeping)](fma-broker-eighteen-site-services.md)
- [FMA Broker Service (XML/STA) and its responsibilities](fma-broker-service.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [VDA high-availability mode for Controller outages](xd7-vda-high-availability-mode.md)
