---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, licensing, sizing]
layer: reference
bron: inside-citrix-fma
---

# Formula for sizing user/device licenses

To estimate the number of user/device licenses needed: **A - C + B = number of user/device licenses**, where A is the total number of users, B is the total number of shared devices, and C is the number of users who will exclusively use those shared devices.

Example from the book: 800 users (A), 300 shared devices (B), 400 users who only use shared devices (C) gives 800 - 400 + 300 = **700 licenses**.

The same formula helps you work out the break-even point where concurrent licenses make more financial sense — concurrent licenses cost roughly **twice** the price of a user/device license.

## Verwante notities

- [Citrix user, device and concurrent licenses](citrix-license-types-user-device-concurrent-2.md)
- [Citrix Server, Farm and Zone Design Trade-offs](citrix-server-farm-zone-design.md)
- [How the license server reassigns user/device licenses](license-server-user-device-reassignment-logic.md)
