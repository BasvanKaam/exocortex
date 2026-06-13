---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [cloud-pc, windows-365, avd, intune, mem, networking]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Cloud PC: MEM-managed vs self-service (durable distinction)

Bas's framing of the two Cloud PC models (originally launched under codename Deschutes, July 2021, on top of the existing AVD architecture):

**MEM-managed Cloud PC** — for organizations already invested in Microsoft Endpoint Manager (Intune) to manage their physical Windows estate. Requires an Intune license per assigned user. Managed via Intune for the OS-and-above layer and via the Azure portal for networking. Admins cannot touch the underlying VM resources, only Windows and applications. Has the same networking flexibility as AVD: full control over routing, VPN, firewall. New to MEM means a (steep) learning curve and extra setup of tenant, network, and Active Directory.

**Self-service Cloud PC** — for individuals and very small businesses; the 'instead of going to Best Buy, subscribe to a cloud PC and have it in an hour' model. No MEM/Intune license, no own tenant/network, no Active Directory. Managed entirely by the end user, like a standalone physical PC. Runs inside Microsoft's own Azure subscription; the network interface sits on a Microsoft-managed network the consumer has zero control over. No dedicated management portal beyond the M365 license portal for assigning licenses and (re)provisioning.

**Shared traits:** every Cloud PC is a persistent, single-user VM dedicated to one user at a fixed price per user per month. The profile is local to the machine, not offloaded via FSLogix. Security agents, licensed apps, and patches see it as an ordinary single-user Windows 10/11 Enterprise device. Multi-session (Windows 10 EVD) is not supported. Purchased through the same M365 channels (E3/E5/Business Premium) as AVD licensing; a physical-device/OEM license does not qualify.

Mental model: AVD is the flexible, fully controllable Azure VDI; Cloud PC is the simpler, more limited, fixed-price cloud PC. Expect organizations to run both side by side.

*Bron: Nerdio-content 'How Nerdio Enhances the Provisioning and Management of Cloud PC' (Blogs).*

## Verwante notities

- [Cloud PC licensing requirements (durable)](cloud-pc-licensing-requirements.md)
- [Cloud PC: MEM-managed vs self-service flavours](cloud-pc-mem-managed-vs-self-service-2.md)
- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-added-value-on-cloud-pc.md)
- [Nerdio self-service portal: delegated machine control for power users](nerdio-self-service-portal-user-control.md)
- [AVD and Cloud PC go hand in hand, pick per use case](positie-avd-en-cloud-pc-gaan-hand-in-hand.md)
- [Windows 365 Cloud PC: What It Is and How It Differs from AVD](w365-cloud-pc-vs-avd-fundamentals.md)
- [Windows 365 Cloud PC - Business vs Enterprise](windows-365-business-vs-enterprise.md)
