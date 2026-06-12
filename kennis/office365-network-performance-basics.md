---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [office365, networking, performance, microsoft, service-front-door]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# Office 365 Network Performance: Service Front Doors and the Basics

When users complain that Office 365 is slow, the cause is usually at the network basics, not the application. Microsoft offers a network onboarding portal that measures connection quality and helps find the nearest Service Front Door.

## Service Front Doors
Service Front Doors are Microsoft's points-of-presence where traffic from your organization or work location enters the Office 365 service. Getting traffic to the closest Front Door is a key optimization factor when setting Office 365 up for an organization. Network disruptions on the path translate directly into a negative user experience.

## Practical tips
- Device choice: use a laptop or tablet capable of running several Office apps side by side; underpowered devices produce a poor experience quickly.
- Browser: not every browser is suited to Office 365; check Microsoft's supported-browser list.
- Desk/location: flex working is everywhere, but poor Wi-Fi coverage at your chosen spot shows up in Office 365 use, especially in audio/video meetings.
- Proxy: Microsoft advises against inserting proxy solutions in the path; if present, let traffic to the Service Front Doors pass through transparently.
- VPN: route Office 365 traffic over the local internet rather than through the VPN tunnel (split tunneling) so it is not degraded.

*Bron: Salomon-IT 'BvK - Office 365 Network Performance Assessment' (CGIT Blogs).*

## Verwante notities

- [Bas's warning: Cloud apps with on-premises backends invite latency trouble](latency-cloud-app-onprem-backend.md)
- [Migrating homefolders and profiles to OneDrive with ShareGate](migrate-homefolders-profiles-to-onedrive-sharegate.md)
- [NetScaler split tunneling: route only corporate traffic through the VPN](netscaler-split-tunneling-concept.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
- [Remote video-conferencing cheat sheet (v1.0, 2020)](remote-conferencing-cheat-sheet-2020.md)
- [Skype for Business Online Retirement Milestones and Teams Migration Concerns](skype-for-business-online-retirement-milestones.md)
