---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, machine-catalog, delivery-group, app-publishing]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XD7 app creation: Catalog then Delivery Group then App

How it worked in XenDesktop 7. 'Application creation' replaced the old 'app publishing' term. The flow:
1. Create a **Machine Catalog** holding server- or desktop-OS machines (virtual or physical; Manual, MCS or PVS provisioned). XD7 added a Remote PC Access catalog type for access to a physical desktop PC.
2. Create a **Delivery Group** and add the Catalog (with at least one available machine).
3. Create the **applications** and assign users.

You cannot create an application without a Delivery Group that has at least one available machine. Apps can be created three ways: inside the Delivery Group wizard, by right-clicking a Delivery Group and choosing Add Application, or from the Applications tab via Create Application (here you add the Delivery Group to the app rather than the other way round).

Desktop OS machines use a single-user ICA stack (PortICA, one session, adds USB/Aero redirection); server OS machines use the multi-user ICA stack (the XenApp stack with a different management interface).

*Bron: blogpost 'How to: Application creation in XenDesktop 7' (2013-07-10), basvankaam.com.*

## Verwante notities

- [XD7 auto-discovers installed apps; App-V replaces Citrix profiling](xd7-app-auto-discovery-and-appv.md)
