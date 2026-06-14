---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, licensing, license-server]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How the Citrix license server allocates user/device licenses

With user/device licenses you don't choose user vs device, the license server decides and always allocates the smallest number of licenses needed, tracked in tables keyed on the device MAC address:

- User 1 logs in first on PC 1 -> gets a **user license**.
- User 2 then logs onto PC 1 -> the server sees multiple users on one device and reassigns it to a **device license**.
- User 1 logging onto PC 2 as well -> server sees one user on multiple machines -> assigns a user license.

Once assigned, a user/device license stays assigned for a minimum of **90 days** before check-in. Concurrent licenses, by contrast, are checked out for the session duration and released at logoff. Licenses can be revoked (e.g. when an employee leaves).

Sizing formula for user/device licenses: A - C + B, where A = total users, B = shared devices, C = users exclusively on shared devices. Concurrent licenses cost roughly twice a user/device license, so the formula also shows where concurrent becomes cheaper.

How it worked then.

*Bron: blogpost 'XenDesktop & XenApp 7.14 multi-type licensing - what it is, how it works and what to be aware of' (2017-06-12), basvankaam.com.*

## Verwante notities

- [Citrix license type vs edition vs consumption model](citrix-license-type-vs-edition.md)
- [Citrix license types: user, device and concurrent](citrix-license-types-user-device-concurrent.md)
- [Microsoft VDA vs RDS licensing for Citrix](microsoft-vda-rds-licensing-for-citrix.md)
- [Multi-type licensing in XenDesktop/XenApp 7.14](multi-type-licensing-714.md)
