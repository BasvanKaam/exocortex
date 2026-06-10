---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, ssl, certificates, wildcard, san]
layer: reference
bron: inside-citrix-fma
---

# Wildcard and SAN certificates

When requesting an SSL certificate you choose lifespan, encryption bit count and certificate type. Two types worth highlighting:

- **Wildcard certificate:** usable on multiple devices/machines without separate certificates. Instead of, say, external.vankaam.local and internal.vankaam.local, you use one `*.vankaam.local` that supports an unlimited number of subdomains.
- **SAN (Subject Alternative Name) certificate:** secures multiple distinct domains, e.g. vankaam.com, basvankaam.org, mydomain.com.

Best practice (per Bas): use third-party certificates for external/inbound connections and internal-CA certificates for internal SSL traffic (e.g. StoreFront to Delivery Controllers); self-signed certificates are handy for test labs and PoCs.

## Verwante notities

- [NetScaler SSL certificates and certificate trust](netscaler-ssl-certificates-and-trust.md)
- [Securing StoreFront connections with SSL and NetScaler](securing-storefront-connections-with-ssl.md)
