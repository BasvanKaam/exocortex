---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [fslogix, wvd, profiles, office-365-container, app-masking, euc]
layer: reference
gedateerd: ja
bron: salomon-wvd
---

# FSLogix: The Five Capabilities Bas Teaches

The FSLogix toolkit as Bas presents it for WVD profile management. Microsoft acquired FSLogix in November 2018 and baked it into WVD; usage is included with the WVD-eligible licenses.

Profile Container: places the entire user profile in a network-based container (standard Windows VHD, no hypervisor). Fast logon, virtually eliminates profile corruption, works alongside other UEM platforms.

Office 365 Container: places the Office 365 cache in a network container, roaming Outlook OST, OneDrive cache, Windows Search and more. Office apps behave as if installed locally.

App Masking: application management without sequencing, snapshotting, packaging or virtualization. All apps live in one base image; only the apps a user is entitled to are revealed; entitlements change in real time. Works with fonts and plugins. Massively reduces the number of gold images to maintain.

Java Redirection: keeps multiple Java versions on one base image, maps the required version per app/website, and uses App Masking to hide the unused versions.

Cloud Cache (added later): a local cache component; apps talk to the local cache, the cache talks to the remote container, so apps keep working through short connection interruptions and re-sync on reconnect.

Bas's stance: at the time, FSLogix was the only profile solution available within WVD. Related: wvd-explained-bvk-framing.

*Bron: Salomon-IT 'Windows Virtual Desktop - SBC-Solutions' (WVD).*

## Verwante notities

- [FSLogix benefits for WVD (and on-premises)](fslogix-benefits-for-wvd-and-on-premises.md)
- [FSLogix Cloud Cache (tech preview, 2018)](fslogix-cloud-cache-2018.md)
- [FSLogix: the three core technologies after the Microsoft acquisition](fslogix-three-core-technologies.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Profile Layering with FSLogix: Mount Instead of Copy](profile-layering-fslogix.md)
- [WVD Explained: Bas's Core Story](wvd-explained-bvk-framing.md)
- [WVD user connection flow and Reverse Connect](wvd-user-connection-flow-and-reverse-connect.md)
- [WVD Whitepaper: The Selling Points](wvd-whitepaper-propositions.md)
