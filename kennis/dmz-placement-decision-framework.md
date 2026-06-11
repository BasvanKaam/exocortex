---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [security, dmz, reverse-proxy, network-architecture, authentication]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# A framework for deciding DMZ vs internal LAN server placement

Bas distilled DMZ-vs-LAN placement into a small set of decision axes that remain useful for any publicly-faced server (the reasoning is not Citrix-specific):

- Can the data be pre-inspected (e.g. SSL offloaded and filtered by a reverse proxy / NetScaler / F5 / ISA-ForeFront) before it hits the machine? Some traffic (like Apple APNS) needs a direct connection and cannot be proxied.
- Can users be pre-authenticated before reaching the machine, or must authentication happen on the host itself? You don't want unauthenticated users or uninspected traffic landing on the internal LAN.
- Does the machine need to be domain-joined? A compromised domain-joined box is far more dangerous than a standalone one.

DMZ basics: it's a buffer/neutral zone between the internet and the internal LAN; single-hop uses two firewalls with the DMZ between, double-hop adds a third firewall and a second DMZ. The ideal DMZ machine is standalone with local accounts only. Workarounds when a box must be domain-aware in the DMZ: a separate DMZ forest/domain with a one-way trust, or an RODC for one-way replication into the DMZ. These principles are durable network-security thinking.

*Bron: blogpost 'Citrix XenMobile MDM... To DMZ or not to DMZ? I might need your help one this one!' (2014-05-26), basvankaam.com.*

## Verwante notities

- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [Getting the XenMobile MDM server out of the DMZ was overdue and underdiscussed](mdm-out-of-dmz-relief.md)
- [NetScaler SSL offload, wildcard and SAN certs](netscaler-ssl-offload-and-cert-types.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
