---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, desktop-player, xenclient, mac, hypervisor, flexcast]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Desktop Player for Mac: XenClient on a type-2 hypervisor

How it worked then (2014): Desktop Player for Mac was built on Citrix XenClient, a FlexCast delivery model of XenDesktop 7.x. It therefore required a XenDesktop infrastructure with at least Enterprise or Platinum licenses, and used the XenClient Synchronizer back-end for central management (image sync, updates, policy, user assignment) over SSL via a local agent. The key difference from XenClient: XenClient is a true type-1 bare-metal hypervisor (not supported on Apple hardware), while Desktop Player for Mac is a type-2 hypervisor installed on top of macOS like any other app. It ran Windows VMs (multiple at once) fully isolated from the Mac, giving Macs the ability to run Windows applications with central management and secure offline access. You switch between VMs and the base Mac with Apple's built-in swipe.

*Bron: blogpost 'Apple MacBooks in the (Windows) Enterprise, do they mix and match?!' (2014-03-06), basvankaam.com.*

## Verwante notities

- [Why was Desktop Player for Mac so quiet?](desktop-player-for-mac-strangely-quiet.md)
