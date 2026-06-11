---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [security, dmz, netscaler, architecture]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Fewer components in the DMZ is more secure (durable principle)

Bas's rule of thumb when fronting the MDM components with a hardware load balancer like NetScaler: "the less components you have in your DMZ the better." Putting a load balancer in front lets you take advantage of additional security functions while keeping the attack surface in the DMZ minimal. The specific products are dated, but the principle (minimise what sits in the DMZ, terminate/inspect at the edge) is durable architecture guidance.

*Bron: blogpost 'XenMobile product overview… and It's nice!' (2013-03-12), basvankaam.com.*

## Verwante notities

- [CVE-2019-19781 Citrix ADC / SD-WAN vulnerability (2020 context)](cve-2019-19781-citrix-adc.md)
- [If traffic is inspected and users authenticated, the DMZ is at least as safe as the LAN](dmz-not-automatically-safer-than-lan.md)
- [A framework for deciding DMZ vs internal LAN server placement](dmz-placement-decision-framework.md)
- [Getting the XenMobile MDM server out of the DMZ was overdue and underdiscussed](mdm-out-of-dmz-relief.md)
- [NetScaler ADC vs NetScaler Gateway editions](netscaler-adc-vs-gateway-2.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [NetScaler HDX Proxy announced to replace the Secure Gateway (Synergy 2016)](netscaler-hdx-proxy-replaces-secure-gateway.md)
- [Intranet Applications: the subnet objects that define split tunneling](netscaler-intranet-applications-object.md)
- [NetScaler SSL offload, wildcard and SAN certs](netscaler-ssl-offload-and-cert-types.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
- [XenMobile MDM moved off the DMZ via NetScaler SSL offloading](xenmobile-ssl-offloading-netscaler.md)
