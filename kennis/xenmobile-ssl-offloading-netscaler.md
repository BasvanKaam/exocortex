---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenmobile, mdm, netscaler, security]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenMobile MDM moved off the DMZ via NetScaler SSL offloading

How it worked then (XenMobile 8.6.1, 2014): the Mobile Device Management (MDM) server gained support for SSL offloading through Citrix NetScaler. This let the MDM server sit on the secure internal network instead of being deployed in the DMZ, which not all competing vendors could offer. It required a NetScaler in place. Bas flagged this as a genuinely strong addition, not a throwaway feature.

*Bron: blogpost '16 random reasons to (at least) consider Citrix XenMobile' (2014-02-12), basvankaam.com.*

## Verwante notities

- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [Getting the XenMobile MDM server out of the DMZ was overdue and underdiscussed](mdm-out-of-dmz-relief.md)
- [Inspecting prerequisites up front saves the whole deployment](prerequisites-discipline-saves-time.md)
