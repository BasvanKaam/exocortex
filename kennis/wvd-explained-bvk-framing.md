---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [wvd, azure, vdi, windows-10-multi-user, euc]
layer: reference
gedateerd: ja
bron: salomon-wvd
---

# WVD Explained: Bas's Core Story

How Bas frames Windows Virtual Desktop for a Dutch IT-pro audience (2019 deck).

What WVD is, in one breath: Windows 10 multi-user, optimized for Office 365 ProPlus, deployable and scalable in minutes, delivering full desktops and/or individual applications, with the integrated security and management of Microsoft 365 (incl. Intune / modern management).

Supported session host OSes: Windows 10, Windows 10 Multi-User, Windows 7, Windows Server 2012 R2 / 2016 / 2019.

The split that matters: WVD is a Microsoft-managed control/management plane (web access, diagnostics, gateway, broker, load balancing). The customer manages the session host VMs, apps and data. Profiles are the only customer-owned state that needs solving.

Load balancing modes:
- Breadth mode (default): spreads users across the host pool.
- Depth-first mode: fills one session host to its max user count before spinning up the next.

Reverse Connect security model: outbound WebSocket connections from the VMs to broker and gateway; bidirectional traffic over https (443); no inbound ports opened on the VM.

Connection flow: user starts RD client -> authenticates to Azure AD -> token returned -> token presented to Web Access, broker queries the DB for entitled resources -> user picks resource, client connects to gateway -> broker sets up host-agent-to-gateway connection, RDP then flows over those connections.

Future-of-the-desktop matrix Bas uses: Windows Server 2019 (multi-user, Win32, Office 2019, LTSC) vs Windows 10 Enterprise multi-user (Win32 + UWP, Office 365 ProPlus, Semi-Annual) vs Windows 10 Enterprise single-user.

Related: see the WVD whitepaper note (wvd-whitepaper-propositions) and the FSLogix profile note for the same era.

*Bron: Salomon-IT 'Windows Virtual Desktop - SBC-Solutions' (WVD).*

## Verwante notities

- [Bet: Windows Virtual Desktop Will Be a Major Force in 2019](bet-wvd-major-impact-2019.md)
- [Christiaan Brinkhoff as 'Mister WVD' and the 2020 WVD framing](christiaan-brinkhoff-mister-wvd.md)
- [Fast, Good, Cheap: You Can Now Pick All Three](fast-good-cheap-pick-three.md)
- [FSLogix benefits for WVD (and on-premises)](fslogix-benefits-for-wvd-and-on-premises.md)
- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [IT as a Utility](it-as-a-utility.md)
- [From RDMI to Windows 10 multi-user: how WVD came to be](wvd-history-rdmi-to-windows-10-multi-user.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [WVD user connection flow and Reverse Connect](wvd-user-connection-flow-and-reverse-connect.md)
- [WVD Whitepaper: The Selling Points](wvd-whitepaper-propositions.md)
