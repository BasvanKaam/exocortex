---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [fslogix, wvd, profile-container, app-masking, reference]
layer: reference
gedateerd: ja
bron: salomon-wvd
---

# FSLogix: the three core technologies after the Microsoft acquisition

Following Microsoft's acquisition of FSLogix, eligible customers get three core technologies (reference, 2019 state):

1. **Profile & Office 365 Container** — a replacement for roaming profiles and folder redirection that places the entire user profile in a network-based (SMB) container. Dramatically speeds up logon and app launch, virtually eliminates profile corruption, and the Office 365 Container roams Outlook OST, OneDrive cache, Skype for Business GAL, and the Windows Search DB. Works alongside existing UEM platforms.
2. **App Masking** — application management without sequencing, packaging, or virtualization. All apps live in the base image; only the apps a user is entitled to are revealed, and entitlements can change in real time. Massively reduces the number of gold images to maintain.
3. **Java Redirection** — protects against vulnerabilities of multiple installed Java versions by mapping specific versions to individual apps or websites, using App Masking to hide unused versions.

FSLogix products can run anywhere, including on-premises.

*Bron: Salomon-IT 'iSense Cloud Infra Summit RDS-WVD' (WVD).*

## Verwante notities

- [Christiaan Brinkhoff as 'Mister WVD' and the 2020 WVD framing](christiaan-brinkhoff-mister-wvd.md)
- [CloudJumper optimization features, platform VM, and pricing (2019)](cloudjumper-optimization-features-and-pricing-2019.md)
- [FSLogix benefits for WVD (and on-premises)](fslogix-benefits-for-wvd-and-on-premises.md)
- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [Baseline Criteria for Modern App and Desktop Delivery (anno 2020)](modern-workplace-delivery-baseline-2020.md)
- [Profile Layering with FSLogix: Mount Instead of Copy](profile-layering-fslogix.md)
- [Profile-on-VHD vs copy-on-login roaming profiles](profile-on-vhd-vs-copy-on-login.md)
