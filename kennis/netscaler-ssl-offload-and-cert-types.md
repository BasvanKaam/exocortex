---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, ssl-offload, wildcard, san-certificate, dmz, mpx]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler SSL offload, wildcard and SAN certs

How it worked on NetScaler (2015), concepts still current:

- SSL Offload virtual server: by default the back-end web server handles all encrypt/decrypt, which is CPU-heavy under load. An SSL Offload vServer delegates handshaking/decrypt/encrypt to the NetScaler, freeing the web servers. After decrypting/inspecting, you can forward as plain HTTP or re-encrypt over HTTPS (end-to-end). For large SSL volumes, an MPX (physical) appliance with a dedicated SSL chip is preferred.
- DMZ placement: the NetScaler doing offload can sit in the DMZ while the web servers stay on the more secure internal network. Note Bas's own correction in the comments: SSL offloading itself does nothing security-wise; the security comes from the additional configuration (authentication, inspection), not from offloading per se.
- Wildcard cert (*.domain.local) covers unlimited subdomains on multiple machines with one cert. Best practice cited: use separate third-party certs for external inbound connections, and internal CA certs (e.g. a wildcard) for internal SSL traffic.
- SAN (Subject Alternative Name) cert secures multiple distinct domains (vankaam.com, mydomain.com, etc.) in one cert.

*Bron: blogpost 'Citrix NetScaler… The basics continued, part four. What about SSL?' (2015-10-01), basvankaam.com.*

## Verwante notities

- [A framework for deciding DMZ vs internal LAN server placement](dmz-placement-decision-framework.md)
- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [Getting the XenMobile MDM server out of the DMZ was overdue and underdiscussed](mdm-out-of-dmz-relief.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
- [SSL certificate trust: who issues, who trusts](ssl-certificates-ca-trust-model.md)
- [SSL handshake: asymmetric to exchange, symmetric to transfer](ssl-handshake-symmetric-asymmetric.md)
- [SSL offloading: termination vs bridging vs acceleration](ssl-offloading-termination-bridging.md)
