---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [desktop-vda, brokeragent, picasvc2, ica-service, hdx]
layer: reference
bron: inside-citrix-fma
---

# Desktop VDA core services: Citrix Desktop Service and Citrix ICA Service

The Desktop VDA consists of multiple FMA core services and plug-ins. Its two main services control all HDX functionality for the duration of the session:

- **Citrix Desktop Service** (BrokerAgent.exe): communicates directly with the Broker service on the Controller and handles initial VDA registration via the CBP (a collection of WCF endpoints). After successful registration it keeps communicating regularly with the Broker service, including various feature plug-ins.
- **Citrix ICA Service** (PicaSvc2.exe, a.k.a. PortICA): implements the actual ICA protocol within the VDA. It receives instructions through the Desktop service protocol from the Broker service. Once notified of a connection, and after AD authentication, ticketing, licensing and HDX policy exchange, the ICA stack starts listening so the launch completes.

Director and Studio also talk to FMA services through WCF over port 80. Older VDAs (5.x and below) need WinRM listening on port 5985/5986 for Director and Studio; with 7.x VDAs this info comes from the monitor plugin through the CBP. Note: PortICA only controls the ICA stack, it doesn't represent the whole stack (the ICA stack, like RDP, is made of many components running in kernel mode).
