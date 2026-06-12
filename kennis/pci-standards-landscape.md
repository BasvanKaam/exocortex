---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [pci, security, compliance, payments, dss, encryption]
layer: reference
gedateerd: nee
bron: cgit-blog
---

# The PCI Standards Landscape: Who Must Comply With What

'PCI-compliant' is thrown around loosely. People often get no further than the abbreviation (Payment Card Industry) and the sense that it touches payments, without grasping what it really means. The PCI Security Standards Council was founded in 2006 by a group of credit card companies to reduce card fraud, and it is not a single standard but a family.

## PCI DSS (Data Security Standard)
The core standard. Defines requirements to protect sensitive payment data and applies to every party in the payment chain: banks, (web) retailers, and payment processors. Anyone who touches sensitive cardholder data (account number, name, expiry, service code) or authentication data (magstripe/chip, card verification codes, PIN). Of all the standards, DSS is the most broadly relevant.

## PCI PTS (PIN Transaction Security)
Predates the PCI organization as Visa's PIN Security Requirements, later folded in. Focused on the cryptographic protection of PIN codes. Most relevant to banks and parties involved in processing payment transactions. DSS only says PINs (even encrypted) must not be stored; PTS governs the actual encryption of PINs using cryptographic hardware and all the (key) management processes around it.

## PCI PTS HSM
Cryptographic hardware is central to the payment chain, designed for secure key storage and for performing cryptographic computations. PCI distinguishes HSMs (Hardware Security Modules) from other crypto hardware. 'Payment HSMs' sit in bank back-office systems; generic HSMs fall outside PTS scope. Where DSS does not require HSMs, PTS does. Payment HSMs must meet one of two standards: NIST FIPS 140-2 or PCI's own PTS-HSM. Relevant to banks, payment processors, and HSM manufacturers.

## PCI PTS POI (Point-of-Interaction)
Devices where PINs are entered, or that only read payment/credit cards: in practice ATMs and payment terminals. Relevant to banks, processors, and POI manufacturers.

## PCI P2PE (Point-to-Point Encryption)
An extension of DSS. End-to-end encryption (from payment terminal to HSM) of the sensitive data DSS specifies, so the data is nowhere present in cleartext. Audience is the DSS audience plus suppliers of these solutions.

## PCI Software-based PIN Entry on COTS
The most recent standard (January 2018), covering PIN entry on generic devices (smartphones/tablets) increasingly used as point-of-sale systems. Aimed mainly at suppliers of these solutions.

## Bottom line
The PCI world is large and complex, but the good news is that not every business handling payments needs to be fully PCI-certified. By number of parties affected, DSS is most relevant; suppliers of payment-infrastructure components deal most with PTS and PTS HSM.

*Bron: Salomon-IT 'BvK - PCI-blog-deel1-v02' (CGIT Blogs).*

## Verwante notities

- [Challenges of getting and staying PCI DSS and PTS certified](pci-dss-pts-certification-challenges.md)
- [Security is a process, not a destination](security-is-a-process-not-a-destination.md)
- [Server hardening can be easy — so there is no excuse](server-hardening-can-be-easy-no-excuse.md)
- [SSL handshake: asymmetric to exchange, symmetric to transfer](ssl-handshake-symmetric-asymmetric.md)
- [Wireless Encryption: WEP, WPA and WPA2](wireless-encryption-wep-wpa-wpa2.md)
