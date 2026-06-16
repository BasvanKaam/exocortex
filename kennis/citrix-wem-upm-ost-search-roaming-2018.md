---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, wem, upm, outlook, ost, vhdx, synergy, application-layering]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix WEM/UPM per-user Outlook search + OST roaming (Synergy 2018)

How it was announced then: at SYN231 Pierre Marmignon announced a WEM/UPM feature (shipping within ~90 days) giving each user a per-user search index database and offline .OST caching, both wrapped into a VHDX container that roams with the profile from one non-persistent machine to another. It worked for XenApp and XenDesktop (session-based and VDI), cross-platform (virtual and physical), enabled by a single checkbox in a UPM policy. Limitations: Outlook only (no OneDrive, OneNote, Skype for Business), and only 32-bit Outlook/Office to start.

Context on the Citrix layering alternatives at that time: Citrix User Layers (part of App Layering) persisted full user profile settings on non-persistent machines but for VDI only (no multi-user Server OS) and were still in beta/labs. Citrix Office 365 Layers were a GA subset of the full User Layer, one or the other at a time, included in/on the image, VDI/desktop only, no OneDrive/S4B/OneNote. User Layers were a Platinum-only feature. Bas's cheat sheet showed you had to mix multiple Citrix products and still needed a third-party product for full coverage.

*Bron: blogpost 'Synergy 2018: Per-user Outlook search indexing and OST caching options' (2018-05-14), basvankaam.com.*

## Verwante notities

- [Citrix acquired Unidesk to own application layering](citrix-acquires-unidesk-layering.md)
- [Citrix's native options still lag third-party containers (May 2018)](citrix-still-behind-third-party-containers-2018.md)
- [Liquidware suite: ProfileUnity, FlexApp, Stratusphere UX (2018)](liquidware-profileunity-flexapp-stratusphere.md)
- [The non-persistent Office 365 / Outlook OST and search-index problem](non-persistent-outlook-search-ost-problem.md)
- [Office 365 cached-mode OST files break on non-persistent desktops](office-365-ost-non-persistent-vdi-problem.md)
- [Office 365 cached mode breaks on non-persistent VDI/RDSH](office365-cached-mode-nonpersistent-problem.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Outlook Online Mode Is Insufficient on VDI/RDSH](outlook-online-mode-insufficient-on-vdi.md)
