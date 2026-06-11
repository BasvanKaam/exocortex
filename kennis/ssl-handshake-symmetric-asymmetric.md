---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [ssl, handshake, encryption, session-key, key-pair]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# SSL handshake: asymmetric to exchange, symmetric to transfer

Durable concept. SSL primarily uses symmetric encryption (one shared key for both encrypt and decrypt) for the bulk data transfer because it is fast and far less resource-intensive. During the initial handshake, asymmetric public-key encryption is used, which is much more CPU-heavy. Symmetric is considered less secure than asymmetric but much faster: a deliberate trade-off.

Key pair: the certificate holds a public and private key. The private key is never shared. The public key goes out during the handshake and is used to encrypt the pre-master secret; only the matching private key can decrypt it.

Handshake flow: Client Hello (SSL version, cipher, session data) to Server Hello (same plus the server's certificate/public key) to client authenticates the cert and creates the pre-master secret, encrypts it with the server's public key to server decrypts with its private key to both derive the master secret to both derive symmetric session keys to encrypted session begins. The handshake's asymmetric work plus optional two-way (client) authentication is the main source of SSL performance overhead - the case for offloading.

*Bron: blogpost 'Citrix NetScaler… The basics continued, part four. What about SSL?' (2015-10-01), basvankaam.com.*

## Verwante notities

- [NetScaler SSL offload, wildcard and SAN certs](netscaler-ssl-offload-and-cert-types.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
