---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [mobility, byod, dual-persona, containerization, mam, security]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Two ways to do Dual Persona: app wrapping vs on-device hypervisor

Dual Persona splits a mobile device into an isolated private space and a corporate space so apps on one side can't talk to apps on the other, and the corporate container can be locked/wiped independently if the device is lost. Two technical approaches:
1. **App wrapping (MAM)**: corporate apps are wrapped with an SDK, gaining encryption, passcode auth, inter-app policies and per-app micro VPNs, then containerized away from personal apps. Vendor-portable and works on iOS.
2. **On-device hypervisor**: a standalone VM on the phone separates corporate from personal. Drawback: needs the OS maker's permission to build a VM on their platform, which is a no-go on Apple iOS, so this route is Android-limited.

Key durable caveat Bas stresses: there is no 100% secure device; technology only goes so far, so pair it with signed user security-policy agreements.

*Bron: blogpost 'BYOD... Beyond the hype' (2013-08-08), basvankaam.com.*

## Verwante notities

- [BYOD has graduated from hype to something you can't ignore](byod-from-hype-to-unavoidable.md)
- [2013 mobile management vendor landscape](byod-vendor-landscape-2013.md)
- [Mobile management acronyms: MDM, MAM, MIM, EMM](mdm-mam-mim-emm-glossary.md)
- [MDX and the MDX Vault: containerizing corporate mobile apps](mdx-mobile-app-containerization.md)
- [Secure the data and access, not the device, and give employees freedom](secure-the-data-not-the-device-give-employees-freedom.md)
