---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, licensing, license-server]
layer: reference
bron: inside-citrix-fma
---

# How the license server reassigns user/device licenses

With user/device licenses the license server always allocates the smallest number of licenses needed, and it dynamically decides the type using tables it keeps (tracked by device MAC address).

Example flow: when user 1 first logs in on PC 1, the server assigns a **user** license to user 1. If user 1 logs off and user 2 logs on to PC 1, the server notices multiple users on PC 1 and reassigns the license to PC 1, turning it into a **device** license. If user 1 then logs onto PC 2, the server sees user 1 on multiple machines and assigns a user license to user 1 — unless PC 2 was also used by multiple users, in which case it keeps a device license for PC 2 and user 1 stays without an assigned license.

Once a user/device license is assigned it stays assigned for a minimum of **90 days** before being checked back in (concurrent licenses, by contrast, are checked in at session end). Licenses can be revoked early — e.g. when an employee leaves — using the Citrix command-line utility **UDADMIN**. License usage data updates every 15 minutes by default; rebooting the license server forces an update. Bram Wolfs built a free GUI around the UDADMIN tool that, among other things, lets you revoke multiple licenses at once.
