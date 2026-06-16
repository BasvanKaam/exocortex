---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [cloud-pc, windows-365, avd, intune, mem, networking, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Cloud PC: MEM-managed vs self-service (durable distinction)

Bas's framing of the two Cloud PC models. Cloud PC (Windows 365, originally launched under codename Deschutes, July 2021) is a Microsoft 365 product that gives each user a persistent, dedicated VM at a fixed price per user per month. It is part of the Microsoft 365 cloud, not Azure consumption, and is built on top of the existing global AVD infrastructure.

**MEM-managed Cloud PC** — for organizations already invested in Microsoft Endpoint Manager (Intune) to manage their physical Windows estate. Requires an additional Intune license per assigned user. Managed via Intune for the OS-and-above layer and via the Azure portal for networking. Admins cannot touch the underlying VM resources, only Windows and applications. Network interfaces are customer-managed, so you keep the same networking flexibility as AVD: full control over routing, VPN, firewall. New to MEM means a (steep) learning curve and extra setup of tenant, network, and Active Directory prerequisites.

**Self-service Cloud PC** — for individuals and very small businesses; the 'instead of going to Best Buy, subscribe to a cloud PC and have it in an hour' model. No MEM/Intune license, no own tenant/network, no Active Directory prerequisites. Managed entirely by the end user, like a standalone physical PC. Runs entirely inside Microsoft's own Azure subscription; the network interface sits on a Microsoft-managed network the consumer has zero control over. No dedicated management portal beyond the M365 admin/license portal for assigning licenses and (re)provisioning. Assign a license and the desktop provisions within an hour.

**Shared traits:** every Cloud PC is a persistent, single-user VM dedicated to one user at a fixed price per user per month. Apps installed persist across logoff/shutdown. The profile is local to the machine, not offloaded via FSLogix. Security agents, licensed apps, and patches see it as an ordinary single-user Windows 10/11 Enterprise device. Multi-session (Windows 10 EVD) is not supported.

**Licensing:** needs a Windows 10/11 Enterprise subscription (same as AVD); a physical-device/OEM license does not qualify. SKUs that include it: M365 Business Premium, E3, E5, Windows 10 Enterprise E3/E5/VDA. Purchased through the same M365 channels as AVD licensing. Intune required only for MEM-managed.

Mental model: AVD is the flexible, fully controllable Azure VDI; Cloud PC is the simpler, more limited, fixed-price cloud PC. Expect organizations to run both side by side.

*Bron: Nerdio-content 'How Nerdio Enhances the Provisioning and Management of Cloud PC' / 'What is, and how Nerdio enhances CPC' (Blogs).*

## Verwante notities

- [AVD vs Cloud PC is a control-vs-simplicity trade-off keyed to your team's Azure skill](avd-vs-cloud-pc-it-depends-on-team-skill.md)
- [Always-on Cloud PCs are wrong for intermittent users; Frontline fills the gap](choose-frontline-vs-enterprise-cloud-pc.md)
- [Cloud PC licensing requirements (durable)](cloud-pc-licensing-requirements.md)
- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [Bas's reframe: is AVD and/or Windows 365 Cloud PC really DaaS?](is-avd-and-windows-365-really-daas.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-added-value-on-cloud-pc.md)
