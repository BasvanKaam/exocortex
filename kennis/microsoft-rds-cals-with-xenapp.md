---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [microsoft, rds, cal, xenapp, xendesktop, licensing]
layer: reference
bron: inside-citrix-fma
---

# Microsoft RDS CALs and the XenApp vs XenDesktop split

When Microsoft RDS (Remote Desktop Services, formerly Terminal Services) is used to deliver apps or desktops, it must be licensed with **RDS CALs** (per user or device). XenApp runs on top of RDS technology and therefore needs RDS CALs. This does not apply to XenDesktop VDI, though RDS technology can also serve desktop-OS VMs on Windows Server 2012/2016 (Microsoft VDI), in which case both VDA and RDS licenses are needed.

Key rule: **Microsoft RDS licenses are needed with Citrix XenApp, not XenDesktop. Microsoft VDA licenses are needed with Citrix XenDesktop, not XenApp.**

Side note: when XenApp is used only to stream packaged applications down to a virtual or physical desktop, no RDS CALs are needed because no actual resources are used on the RDSH server.

## Verwante notities

- [Citrix license types: user, device and concurrent](citrix-license-types-user-device-concurrent.md)
- [Citrix Service Provider (CSP) program](citrix-service-provider-program.md)
- [From Terminal Services to AVD - The Multi-User History](history-terminal-services-to-avd.md)
- [Microsoft App-V components and licensing with Citrix](microsoft-app-v-with-citrix.md)
- [Microsoft CDL (Companion Desktop License)](microsoft-cdl-companion-device-license.md)
- [Microsoft SPLA and why true DaaS is restricted](microsoft-spla-daas-licensing-restriction.md)
- [Microsoft VDA licenses and Software Assurance](microsoft-vda-license-software-assurance.md)
- [Microsoft VDA vs RDS licensing for Citrix](microsoft-vda-rds-licensing-for-citrix.md)
- [Server VDA vs Desktop VDA: the often-overlooked new component](server-vda-vs-desktop-vda.md)
- [VDA license rules and Microsoft licensing nuances](vda-license-rules-microsoft-licensing.md)
