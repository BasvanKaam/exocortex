---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [ssl, certificates, ca, pki, self-signed, trust]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# SSL certificate trust: who issues, who trusts

Durable concept. A certificate is always issued and signed by a Certificate Authority (CA). There are three sourcing routes:

- Internal domain PKI: you stand up your own CA and hand out certs. Cheap but every client must be made to trust your internal CA, which can be a daunting task at scale for external clients.
- Self-signed: the machine signs its own cert and is effectively its own CA (it can't issue certs to other machines). Clients must explicitly trust that machine.
- Third-party trusted CA (GoDaddy, VeriSign, GlobalSign, DigiCert, etc.): browsers ship trusting these CAs by default, so no warnings. You pay, and the CA runs an extensive verification program before issuing - which is exactly why browsers trust them.

Trust rule: when a client connects to a resource, the resource presents its cert; the client must trust the CA that issued and signed it, or the user gets a security warning. This applies machine-to-machine too (e.g. NetScaler trusting the CA that signed a StoreFront cert).

*Bron: blogpost 'Citrix NetScaler… The basics continued, part four. What about SSL?' (2015-10-01), basvankaam.com.*

## Verwante notities

- [NetScaler SSL offload, wildcard and SAN certs](netscaler-ssl-offload-and-cert-types.md)
