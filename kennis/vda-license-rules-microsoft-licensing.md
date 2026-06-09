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
