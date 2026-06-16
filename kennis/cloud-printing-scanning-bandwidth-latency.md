---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-16
tags: [printing, scanning, cloud, rdsh, vdi, latency, bandwidth]
layer: reference
gedateerd: nee
bron: inside-citrix-book
---

# Printing and scanning are the trap when hosting RDSH/VDI in the cloud

When the RDSH/VDI back-end moves to the cloud but printers and scanners stay local with the user, every print and scan job crosses the WAN. Bandwidth and latency limits make this a recurring pain point that is easy to forget during cloud planning.

Also a data-locality issue more broadly: many applications do not function well when physically separated from their data, and in practice apps are often separated from their data. Plan for where data lives relative to where it is consumed.

*Bron: Inside Citrix (2016), 'Inside Citrix Ch3 - Is the FMA still relevant (cloud vs on-prem)'.*

## Verwante notities

- [Why RDS Easy Print falls short for cloud/remote printing](easy-print-limitations-cloud.md)
- [Hybrid Latency and the Region-Choice Pitfall](hybrid-latency-region-choice-pitfall.md)
- [Bas's warning: Cloud apps with on-premises backends invite latency trouble](latency-cloud-app-onprem-backend.md)
- [Printing is the perennial pain admins shouldn't have to focus on](printing-is-a-perennial-euc-pain.md)
- [Multi-site brokering is easy, user-data locality is the catch](user-data-locality-is-the-catch-in-multisite.md)
