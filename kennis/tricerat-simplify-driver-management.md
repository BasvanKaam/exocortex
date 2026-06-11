---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, tricerat, direct-ip-printing, drivers, self-service]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Tricerat Simplify: central driver management for direct IP printing (2018)

How it worked in 2018. Tricerat's Simplify Driver Management keeps the benefits of direct IP printing while removing the decentralized-management pain. At logon the workstation queries a central SQL database that holds all assigned printers (by user, IP, machine) and their associated drivers; the user receives the printers they are entitled to plus any new or updated drivers, and the print queue is created locally so all print traffic goes directly to the device's IP, no servers or services in the path. From a remote site the only traffic back to the datacenter is that database query (plus a driver if new/updated), keeping bandwidth low and print traffic local.

Drivers are imported into the database via an import tool that auto-detects local drivers (imported per-driver via a toggle) and tracks version changes. Printer objects are created in the Tricerat Simplify console (name, IP, 32- and 64-bit drivers) and assigned by IP/range, machine name, user or group with visual AD integration. Assignment modes: explicit (statically assigned, user has no control) or "permission to use" (user handpicks devices via a self-service printer app). Users still get the native manufacturer preferences dialog.

*Bron: blogpost 'Direct IP printing made manageable with Tricerat' (2018-09-18), basvankaam.com.*

## Verwante notities

- [Print driver isolation: None, Shared, Isolated](print-driver-isolation-modes.md)
- [Printing is the perennial pain admins shouldn't have to focus on](printing-is-a-perennial-euc-pain.md)
- [Printing is still critical; Citrix deprioritized it for cloud](printing-still-critical-citrix-deprioritized-it.md)
