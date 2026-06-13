---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [windows-365, cloud-pc, avd, intune, mem, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Cloud PC: MEM-managed vs self-service flavours

Cloud PC (Windows 365, 2021 codename "Deschutes") is a Microsoft 365 product that gives each user a persistent, dedicated VM at a fixed price per user per month. It is part of the Microsoft 365 cloud, not Azure consumption, and is built on the existing global AVD infrastructure. Apps installed persist across logoff/shutdown; the profile is local to the machine, so no FSLogix. The VM presents as a single-user, traditional Windows 10/11 Enterprise device to security agents, app licensing, and patching. Windows multi-session (EVD) is not supported. Purchased through the same E3/E5 channels as AVD.

Two flavours, each with trade-offs:

- **MEM-managed**: needs an additional Intune license per user. Network interfaces are customer-managed, so you keep full control over routing, VPN, firewall, just like AVD. The on-ramp for shops that already run Intune for physical devices. Setting up tenant, network, AD prerequisites takes attention.
- **Self-service**: no Intune license, no own tenant/network, no AD prerequisites. Runs entirely inside Microsoft's Azure subscription. Assign a license in the M365 admin portal and the desktop provisions within an hour. The catch: network interfaces sit on a Microsoft-managed network you have zero control over, and there is no dedicated management portal beyond handing out licenses.

Licensing: needs a Windows 10/11 Enterprise subscription (same as AVD); a physical-device OEM license does not qualify. SKUs that include it: M365 Business Premium, E3, E5, Windows 10 Enterprise E3/E5/VDA. Intune required only for MEM-managed.

*Bron: Nerdio-content 'What is, and how Nerdio enhances CPC' (Blogs).*

## Verwante notities

- [Cloud PC licensing requirements (durable)](cloud-pc-licensing-requirements.md)
- [Cloud PC: MEM-managed vs self-service (durable distinction)](cloud-pc-mem-managed-vs-self-service.md)
- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-value-on-top-of-cloud-pc.md)
- [Windows 365 Cloud PC: What It Is and How It Differs from AVD](w365-cloud-pc-vs-avd-fundamentals.md)
