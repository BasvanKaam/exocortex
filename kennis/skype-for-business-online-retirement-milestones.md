---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [office-365, teams, skype-for-business, migration, lifecycle]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# Skype for Business Online Retirement Milestones and Teams Migration Concerns

Bas's CGIT blog ('Bye Bye Skype for Business Online, hello Teams') on Microsoft winding down Skype for Business Online (SfB) in favour of Teams. The licensing/availability milestones he calls out (verify against Microsoft lifecycle docs before reuse, the draft extraction is partly garbled):

- From August 2018 the standalone P1 SfB Online plan could no longer be purchased.
- As of 1 July the standalone P2 variant was no longer available either.
- For new Office 365 tenants, adding users to SfB Online is no longer possible; existing tenants already using it keep the option for now.
- The on-premises Skype for Business server is not retired yet, but he expects movement there 'very soon'.

Practical migration notes he raised:
- Roadmap changes were still pending so Teams could match all functionality users were used to in SfB, e.g. chatting with consumer-Skype contacts and the presence indicator that feeds Outlook and SharePoint.
- Telephony users should take steps to keep telephony working correctly; this may require changes to the Session Border Controller and firewall when IP-range exclusions are used (parameters were expected to adjust automatically).
- Beyond the technical change, the organisational challenge is rolling Teams out internally; Teams offers far more capability, which can work for or against you.

*Bron: Salomon-IT 'Blog SBC - Blog CGIT - Afscheid Skype for Business Online V2 - BvK' (CGIT Blogs).*

## Verwante notities

- [Choose Collaboration Tools by Purpose, Not Default](choose-collaboration-tool-by-purpose.md)
- [Office 365 Network Performance: Service Front Doors and the Basics](office365-network-performance-basics.md)
- [Remote video-conferencing cheat sheet (v1.0, 2020)](remote-conferencing-cheat-sheet-2020.md)
- [Teams in-browser video was gated to Edge user-agent (2019)](teams-browser-video-edge-gating-2019.md)
