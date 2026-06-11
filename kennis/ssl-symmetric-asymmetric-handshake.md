---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [ssl, cryptography, handshake, performance]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Why the SSL handshake is the expensive part (asymmetric vs symmetric)

An SSL session uses two kinds of crypto:
- **Asymmetric (public key)** encryption is used only during the **handshake**, to authenticate the server (and the client under two-way auth) and establish the connection. It is the most resource-intensive phase.
- **Symmetric** encryption (a single shared key) is used for the bulk data transfer once the connection is established. It is far faster and less CPU-heavy, but considered less secure, a deliberate trade-off.

Because the asymmetric handshake is where the CPU cost concentrates, SSL offloading and acceleration target exactly that phase. This is a durable explanation of why TLS/SSL session setup is comparatively expensive.

*Bron: blogpost 'NetScaler SSL Offloading for XenMobile MDM... Finally!' (2014-01-27), basvankaam.com.*
