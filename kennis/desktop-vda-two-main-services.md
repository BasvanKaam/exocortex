---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, brokeragent, picasvc2, ica-service, hdx]
layer: reference
bron: inside-citrix-fma
---

# Desktop VDA core services: Citrix Desktop Service and Citrix ICA Service

The Desktop VDA consists of multiple FMA core services and plug-ins. Its two main services control all HDX functionality for the duration of the session:

- **Citrix Desktop Service** (BrokerAgent.exe): communicates directly with the Broker service on the Controller and handles initial VDA registration via the CBP (a collection of WCF endpoints). After successful registration it keeps communicating regularly with the Broker service, including various feature plug-ins.
- **Citrix ICA Service** (PicaSvc2.exe, a.k.a. PortICA): implements the actual ICA protocol within the VDA. It receives instructions through the Desktop service protocol from the Broker service. Once notified of a connection, and after AD authentication, ticketing, licensing and HDX policy exchange, the ICA stack starts listening so the launch completes.

Director and Studio also talk to FMA services through WCF over port 80. Older VDAs (5.x and below) need WinRM listening on port 5985/5986 for Director and Studio; with 7.x VDAs this info comes from the monitor plugin through the CBP. Note: PortICA only controls the ICA stack, it doesn't represent the whole stack (the ICA stack, like RDP, is made of many components running in kernel mode).

## Verwante notities

- [PortICA / picaSvc2.exe: the critical VDA ICA service](portica-picasvc2-service.md)
- [Server VDA vs Desktop VDA: the often-overlooked new component](server-vda-vs-desktop-vda.md)
- [Two VDA types and the single-user vs multi-user ICA stack](two-vda-types-ica-stack-difference.md)
- [What happens inside the VDA during launch (PortICA/ICA service)](vda-internals-during-launch.md)
- [The VDA: client-side component, services and registration](vda-overview-services-and-registration.md)
- [VDA registration and how to verify it](vda-registration-and-verification.md)
- [VDA registration: auto-update, fallback locations and the CBP](vda-registration-process.md)
