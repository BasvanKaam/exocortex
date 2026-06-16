---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [windows-365, avd, intune, licensing, dated]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Windows 365 Cloud PC: What It Is and How It Differs from AVD

Bas's framing of Windows 365 (announced at Microsoft Inspire, 14 July 2021) for an AVD-literate audience. The clean mental model below is the durable part; specific SKUs and limits are version-dated.

## The mental model
- A Cloud PC is a persistent, single-user VM at a fixed price per user per month. It is part of the Microsoft 365 cloud, purchased through the same channels as E3/E5, not metered Azure consumption.
- It is built on the same global Azure Virtual Desktop infrastructure underneath, but it behaves and is managed like a physical Windows device.
- Profile is local to the machine; no FSLogix offload to a file share. Apps installed by the user persist across logoff/shutdown.
- Every security agent, licensed app, and patch sees it as a normal single-user Windows 10/11 Enterprise device. That sameness is the whole point: manage Cloud PCs alongside physical machines and, over time, replace physical machines with them.
- Multi-session (EVD) Windows 10/11 is not supported; single-session only. Gen 2 VMs only.

## Licensing
- Requires a Windows 10/11 Enterprise subscription, plus an Intune license for Enterprise Cloud PCs. Same Windows subscription requirement as AVD.
- A physical-device license (e.g. OEM) does not qualify; only an M365 subscription to Windows. SKUs that include it: M365 Business Premium, E3, E5, Windows 10 Enterprise E3/E5/VDA.

## Enterprise vs Business
- Enterprise: managed via Intune/Endpoint Manager + Azure portal for networking; supports custom images and on-prem AD (Hybrid Azure AD Join), and has AVD-equivalent networking flexibility.
- Business: no dedicated management portal beyond the M365 portal for handing out licenses and kicking off provisioning. Ongoing management falls to the end user or a third-party tool.

## Bas's positioning of the value
- If you already run (or are considering) AVD, W365 sits alongside it cleanly: subscription-based, no minimums, and "if it doesn't work out, you just hand them back over to Microsoft" — a core advantage of cloud. Nerdio Manager layers extra management (image management, autoscaled file shares, side-by-side AVD + W365 from one interface) on top of the native service for both Enterprise and Business.

*Bron: Nerdio-content 'w365 Cloud PC - getting started' ((root)).*

## Verwante notities

- [Cloud PC licensing requirements (durable)](cloud-pc-licensing-requirements.md)
- [Cloud PC: MEM-managed vs self-service (durable distinction)](cloud-pc-mem-managed-vs-self-service.md)
- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [AVD and Cloud PC go hand in hand, pick per use case](positie-avd-en-cloud-pc-gaan-hand-in-hand.md)
- [Windows 365 and AVD Are Complementary, Not Competing](positie-w365-and-avd-coexist.md)
- [Windows 365 License Optimization: The Three Levers](w365-license-optimization-method.md)
- [Windows 365 Cloud PC - Business vs Enterprise](windows-365-business-vs-enterprise.md)
- [Windows 365 Cloud PC](windows-365-cloud-pc.md)
- [Windows 365 Reserve (Cloud PC panic button)](windows-365-reserve-explainer.md)
