---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, ssl, certificates, ca, security]
layer: reference
bron: inside-citrix-fma
---

# NetScaler SSL certificates and certificate trust

When a remote user connects to a NetScaler acting as a secure gateway, the NetScaler presents an **SSL certificate** to prove its identity. Because certificates can be forged, a trust mechanism is needed: certificates are issued and signed by a **Certificate Authority (CA)**, and the CA that issued the certificate must be trusted by the connecting client. If trusted, the connection proceeds; if not, the user gets a security warning.

Certificates can be: issued by your own internal **PKI/CA** (can also be done on the NetScaler), **self-signed** (the machine trusts itself and can't issue to others), or purchased from a trusted external third-party CA. The advantage of well-known third-party CAs (e.g. GoDaddy, Verisign, GlobalSign, DigiCert) is that major browsers already trust them by default, thanks to their extensive verification programmes. Cost varies by vendor, certificate type and validity period.

The same trust model applies internally — e.g. when the NetScaler connects to a StoreFront server, it must trust the CA that signed StoreFront's certificate. If you use an internal CA or self-signed certificates, you must make all users/devices trust that CA, which can be a daunting task depending on the number and type of external clients.

## Verwante notities

- [NetScaler SNIP, STA tickets and certificate practice](netscaler-snip-and-sta.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [Securing StoreFront connections with SSL and NetScaler](securing-storefront-connections-with-ssl.md)
- [Wildcard and SAN certificates](wildcard-and-san-certificates.md)
