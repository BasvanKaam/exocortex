---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [licensing, vda, rds, software-assurance, daas]
layer: reference
bron: inside-citrix-fma
---

# VDA license rules and Microsoft licensing nuances

Licensing details Bas captures:
- Microsoft RDS licenses go with Citrix XenApp (not XenDesktop); Microsoft VDA licenses go with XenDesktop (not XenApp).
- Accessing a Windows desktop OS from a physical PC (not a server-hosted VM) needs no Windows VDA license; VDA licenses do not apply to XenApp.
- Software Assurance is technically an upgrade of existing (usually OEM) licenses — so you cannot have SA on thin clients (no existing license to upgrade) and must buy a VDA license instead. SA benefits allow up to four VDI VMs or one physical machine running a Windows desktop OS.
- For 'true' cloud-based VDI, customers must provide their own Windows desktop OS licenses; a Service Provider is not allowed to sell these. This Microsoft licensing restriction is why true desktop-OS DaaS at acceptable cost remains hard, and why most DaaS is RDSH/XenApp-based (shared desktop) in the back-end.

## Verwante notities

- [Bas's 2018 reframe: true VDI from the cloud and Microsoft licensing](daas-true-vdi-licensing-evolution.md)
- [Microsoft CDL (Companion Desktop License)](microsoft-cdl-companion-device-license.md)
- [Microsoft RDS CALs and the XenApp vs XenDesktop split](microsoft-rds-cals-with-xenapp.md)
- [Microsoft SPLA and why true DaaS is restricted](microsoft-spla-daas-licensing-restriction.md)
- [Microsoft VDA licenses and Software Assurance](microsoft-vda-license-software-assurance.md)
- [Microsoft VDA vs RDS licensing for Citrix](microsoft-vda-rds-licensing-for-citrix.md)
- [VDA install options and supported operating systems](vda-install-options-and-supported-os.md)
- [Windows server/desktop OS licensing and App-V (MDOP)](windows-server-desktop-os-licensing-mdop.md)
