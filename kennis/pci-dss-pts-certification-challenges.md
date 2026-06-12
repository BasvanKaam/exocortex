---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [pci, compliance, security, dss, pts, hsm, cryptography, key-management]
layer: reference
gedateerd: nee
bron: cgit-blog
---

# Challenges of getting and staying PCI DSS and PTS certified

Part 2 of a PCI (Payment Card Industry) series. Possible partner/guest content (closes with a contact pointer to Avensus High Grade Security). Captured for the durable knowledge.

Why certify at all: the easy answer is that it is mandatory if you operate in the payments world, and non-compliance can lead directly to fines. The better answer is to do it for your own benefit — fewer security incidents, less reputational damage, and a stronger competitive position from a better security reputation.

DSS certification:
- DSS requirements are not rocket science and would fit any company's security plan (published at pcisecuritystandards.org).
- A key control for protecting cardholder data is cryptography, with the corresponding requirements for proper key management.
- Certification requires passing an audit by an independent party (QSA = Qualified Security Assessor).
- The biggest lever to simplify certification is scope reduction: know exactly which systems and applications process and/or store cardholder data, then segregate those systems from the rest of the infrastructure to shrink audit scope.
- Run a self-assessment first — a questionnaire to gauge current security level and find gaps — before the official audit.

PTS certification:
- Scope is the encryption of PIN codes using cryptographic hardware and all the (key) management processes around it.
- Certification is done by the individual credit card companies, not by the PCI organisation.
- Main stumbling blocks: HSMs that are not (fully) PCI compliant (hardware and standard firmware are usually certified, but customer-specific firmware often is not, and certifying it is expensive); lack of crypto-agility in payments (legacy algorithm support prevents HSMs from running in PCI mode); poor documentation of processes/procedures and the evidence that they are actually followed (time pressure and daily chaos undermine key-management documentation); and a shortage of experienced, qualified key managers, since key management is a real specialism.

Future direction to make this easier: use standard HSMs without customer-specific firmware as much as possible, and ultimately outsource these sensitive processes or use cloud services (HSM-as-a-Service and/or Key-Management-as-a-Service). Neither happens overnight, but both belong on the long-term agenda. Practical HSM examples named: nCipher, PayShield, Luna; relevant standards/topics: FIPS 140-2 vs PCI HSM, Key Block, HSM in PCI mode, Key Exchange TR-31.

*Bron: Salomon-IT 'PCI-blog-deel2-v01' (CGIT Blogs).*

## Verwante notities

- ["As a Service" Is a Go-To-Market Move, Not Necessarily a New Product](as-a-service-is-a-go-to-market-not-a-product.md)
- [LAPS for managing local admin passwords](laps-local-admin-password-management.md)
- [The PCI Standards Landscape: Who Must Comply With What](pci-standards-landscape.md)
- [Security is a process, not a destination](security-is-a-process-not-a-destination.md)
- [Server hardening can be easy — so there is no excuse](server-hardening-can-be-easy-no-excuse.md)
