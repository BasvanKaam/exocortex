---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, xendesktop, delivery-controller, vda]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The FMA's 10 (or 12) primary services and their roles

How it worked then (XenDesktop 7.x): the Flex Management Architecture is service-oriented, with ten primary services on the Delivery Controller, plus two on each Desktop OS VDA (Desktop/Broker service and PortICA service), making twelve total in a VDI deployment. Roles:

- Broker (XML) service - brokers sessions, resource enumeration, STA ticket creation/verification, user validation, disconnected sessions.
- Configuration service - all FMA services register with it on startup; handles inter-service communication ('the glue').
- Identity service - manages AD computer accounts for XA/XD machines.
- Configuration Logging service - logs all config changes and admin activity; can block changes when its DB is unreachable.
- Delegated Administration service - manages delegated admin permissions.
- Machine Creation service (MCS) - creates virtual machines only (use PVS for physical).
- Host service - manages connections to physical hosts and the hypervisor (vSphere, XenServer or Hyper-V).
- Environment Test service - runs Site tests (from Studio).
- Monitor service - produces alerts/warnings shown in Studio/Director.
- StoreFront service - manages the StoreFront deployment from Studio.
- (VDA) Desktop service and (VDA) PortICA service - handle authentication ticket/credential exchange and the ICA connection.

*Bron: blogpost '12 services that make up the Citrix XenDesktop Flex Management Architecture' (2015-03-26), basvankaam.com.*

## Verwante notities

- [Check FMA service health with PowerShell, not just Director](check-fma-services-with-powershell.md)
- [The PortICA service (PicaSvc2.exe) and why it's excluded from default traces](portica-picasvc2-ica-service-role.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
