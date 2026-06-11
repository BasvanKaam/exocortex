---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [ssl, netscaler, offloading, security, networking]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# SSL offloading: termination vs bridging vs acceleration

SSL offloading moves the CPU-intensive handshake/decrypt/encrypt work off the web server onto a dedicated device (e.g. a NetScaler), which can also sit in the DMZ while the protected web servers stay on the internal network.

The main approaches:
- **SSL Termination**: traffic is decrypted and inspected at the appliance, then sent to the web server **unencrypted**. Fast and frees the server, but the internal hop is plaintext, which some flag as a security risk.
- **SSL Bridging**: like termination but re-encrypts before sending to the web server, so the internal hop stays encrypted. More secure, but the web server still does decrypt/encrypt work, so less of a performance win.
- **SSL Acceleration**: a physical PCI/SCSI co-processor card in the server that offloads the asymmetric-crypto part of the handshake. Processing still happens on that one server, and it applies to a single server only, unlike termination/bridging which can front multiple servers.

NetScaler terminology differs from generic networking: Citrix "SSL Offloading" maps to termination (with an end-to-end re-encrypt variant Citrix recommends), while a NetScaler SSL Bridge passes traffic through still-encrypted and uninspected, which Citrix advises avoiding. Core principle: SSL offloading is always a trade-off between speed and security. This concept is durable.

*Bron: blogpost 'NetScaler SSL Offloading for XenMobile MDM... Finally!' (2014-01-27), basvankaam.com.*

## Verwante notities

- [NetScaler SSL offload, wildcard and SAN certs](netscaler-ssl-offload-and-cert-types.md)
