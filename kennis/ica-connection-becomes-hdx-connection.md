---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, ica, hdx, protocol, terminology]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# ICA connection renamed HDX connection (terminology shift, 2013)

Bas notes the protocol itself did not disappear: once the client receives an ICA configuration file from StoreFront (after authentication and enumeration), it sets up a direct connection to the desktop or server. That connection, "formerly known as an ICA connection, is now called an HDX connection," reflecting the new delivery and user-experience options layered on top. Useful context for why Citrix docs of this era flip between 'ICA' and 'HDX' for what is essentially the same on-the-wire connection.

*Bron: blogpost 'Post Excalibur remarks' (2013-04-10), basvankaam.com.*

## Verwante notities

- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [Citrix origins: from Citrus Systems to WinFrame, and the birth of ICA](citrix-origins-and-ica-birth.md)
- [HDX extends ICA, it does not replace it](hdx-extends-ica-not-replaces.md)
- [The PortICA service (PicaSvc2.exe) and why it's excluded from default traces](portica-picasvc2-ica-service-role.md)
- [How Microsoft RDP descended from Citrix's ICA](rdp-descended-from-citrix-ica.md)
- [Single-user vs multi-user ICA stack (PortICA) and what it unlocks](single-vs-multi-user-ica-stack.md)
- [StoreFront authenticates locally, Web Interface delegates via XML](storefront-vs-webinterface-auth-flow.md)
