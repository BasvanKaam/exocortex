---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-studio, delegated-administration, host-connection, licensing, appdna, app-v]
layer: reference
bron: inside-citrix-fma
---

# Citrix Studio Configuration sub-nodes

Under the Configuration node:

- Administrators: configure delegated administration on three pillars: (1) Scopes (a collection of objects a user may administer, e.g. connections, Catalogs, Delivery Groups), (2) the Administrator (the person executing tasks), (3) Roles (a set of permissions granted, built-in or custom).
- Controllers: shows active and non-active Delivery Controllers. 'Last Updated' shows '0 minutes ago' when healthy, because Controllers keep a continuous connection to the Central Site database via a heartbeat sent every 20 seconds with a default 40-second timeout.
- Hosting: add/configure Host Connections (the underlying hypervisor or cloud platform), one of the nine main FMA components; it completes the list.
- Licensing: shows active licenses, expiry, type, model (user/device or concurrent), Subscription Advantage date, license server name and port, usage and administrators; allocate/add licenses, change server, edit product edition.
- StoreFront: add an existing StoreFront deployment to configure Receiver on Delivery Group machines (does not enable StoreFront management from Studio).
- App-V Publishing: add/remove Microsoft App-V Management and Publishing servers. As of 7.8 you can add App-V packages directly via a UNC path; Ctxappvlauncher.exe handles it.
- AppDNA: integrated into Studio as of 7.8 but still installed as a separate product. Simplifies application management (Discover, Model, Automate, Manage); reports compatibility and remediation, can auto-create MSI packages (Platinum only).
