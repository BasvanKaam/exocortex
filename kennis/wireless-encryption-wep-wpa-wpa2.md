---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [wireless, wifi, security, encryption, fundamentals]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Wireless Encryption: WEP, WPA and WPA2

Three generations of Wi-Fi encryption, weakest to strongest.

- WEP: based on a shared secret that is set once and rarely (if ever) changed. Fairly quick to crack, so not secure.
- WPA: uses TKIP (Temporal Key Integrity Protocol), which changes the encryption key on every transmitted frame.
- WPA2: uses AES, regarded as effectively secure and practically unhackable.

The progression to per-frame keying and then to AES is the durable principle here; WPA2/AES was the strong option at the time of writing.

*Bron: Core Knowledge doc 'Wirreless Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DHCP security threats](dhcp-security-threats.md)
- [Kerberos V5 Authentication](kerberos-v5-authentication.md)
- [The PCI Standards Landscape: Who Must Comply With What](pci-standards-landscape.md)
- [Frame security guidance as a living starting point, not a final word](security-checklist-as-living-starting-point.md)
- [SSL handshake: asymmetric to exchange, symmetric to transfer](ssl-handshake-symmetric-asymmetric.md)
- [Why the SSL handshake is the expensive part (asymmetric vs symmetric)](ssl-symmetric-asymmetric-handshake.md)
- [The Weakest Link Is You (Security Training War Story)](weakest-link-is-you-security-training.md)
- [Zero Trust Security Model](zero-trust-model.md)
