---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, gateway, storefront, authentication, sta, ica]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler Gateway remote-access traffic flow

How it worked then (Citrix remote access via NetScaler Gateway + StoreFront):

1. External user connects to the Gateway vServer's VIP over 443 (preferred over 80).
2. Authentication on the NetScaler in the DMZ: credentials forwarded via NSIP to Active Directory, ideally with two-factor (e.g. SMSPasscode tokens).
3. Once authenticated, the user connects through a SNIP to the internal StoreFront server, which enumerates apps/desktops.
4. Enumerated resources travel back through the Gateway vServer to the user.
5. On launch, StoreFront generates an .ICA file sent to the device to connect directly to the XenApp/XenDesktop server; the Gateway validates the session against the STA file.

Security guidance: prefer authentication in the DMZ over passing unauthenticated users to internal StoreFront, and always use 443 over 80.

*Bron: blogpost 'Citrix NetScaler Gateway, the basics!' (2014-09-23), basvankaam.com.*

## Verwante notities

- [The STA only comes into play when traffic traverses a NetScaler](citrix-sta-only-with-netscaler.md)
- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [External launch process: Hosted Shared Desktop via NetScaler](external-launch-process-hsd-netscaler.md)
- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [ISA Server 2004/2006 Configuration Concepts](isa-server-configuration-concepts.md)
- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [Content switching policy types and Unified Gateway](netscaler-cs-policy-types-and-unified-gateway.md)
- [NetScaler HDX Proxy announced to replace the Secure Gateway (Synergy 2016)](netscaler-hdx-proxy-replaces-secure-gateway.md)
- [NetScaler split tunneling: route only corporate traffic through the VPN](netscaler-split-tunneling-concept.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
- [The Secure Ticket Authority (STA)](secure-ticket-authority-sta.md)
