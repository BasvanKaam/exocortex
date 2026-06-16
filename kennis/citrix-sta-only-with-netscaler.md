---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, sta, netscaler, broker, ica, launch]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The STA only comes into play when traffic traverses a NetScaler

The Secure Ticket Authority (STA) runs as part of the Broker Service on the Delivery Controller. It is only used during a resource launch when the connection goes through a NetScaler Gateway (externally, or internally if you route internal traffic through the gateway). For purely internal launches handled by StoreFront you do not need to worry about the STA or its tickets.

Mechanics, as it worked then: the STA ticket is generated at launch time (not during enumeration), gets embedded in the launch.ica file, and the Delivery Controller holds it in memory for a configurable period. When the session is established the NetScaler checks the ticket back against the same STA service that issued it; once verified the ticket is deleted. The STA guarantees the user was authenticated at the web tier and authorises the NetScaler ICA proxy to open an inside connection, without the outside knowing anything about the internal network.

Important config rule: NetScaler and StoreFront (or Web Interface) must point to the exact same XML/STA service(s) / Delivery Controller(s).

*Bron: blogpost 'Demystifying the Citrix XenApp logon, enumeration and launch steps' (2016-12-19), basvankaam.com.*

## Verwante notities

- [Broker Service: XML, STA and the Principal Broker](broker-service-xml-sta-principal.md)
- [The Broker Service bundles brokering, XML and STA in one process](citrix-broker-service-three-roles.md)
- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [NetScaler HDX Proxy announced to replace the Secure Gateway (Synergy 2016)](netscaler-hdx-proxy-replaces-secure-gateway.md)
- [NetScaler SNIP, STA tickets and certificate practice](netscaler-snip-and-sta.md)
- [The Secure Ticket Authority (STA)](secure-ticket-authority-sta.md)
