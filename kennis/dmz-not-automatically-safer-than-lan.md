---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [security, dmz, positie, network-architecture]
bron: basvankaam-blog
---

# If traffic is inspected and users authenticated, the DMZ is at least as safe as the LAN

Bas openly changed his mind in public. Four months earlier he'd argued SSL offloading let you put the XenMobile MDM server on the more-secure internal LAN. Here (May 2014) he reconsiders: 'I must admit that the idea of placing the MDM server in the DMZ doesn't sound that bad after all.'

His emerging position: if a publicly-faced machine sits behind a reverse proxy that already inspects data and pre-authenticates users, placing it on the internal LAN buys you little, and the DMZ may be better. 'The way I see it, they're as secure on your DMZ as they will be on your internal corporate LAN.' His clinching argument is blast radius and an extra barrier: 'machines being compromised in your DMZ potentially (unless domain joined) only affect other machines in your DMZ, machines compromised on your corporate LAN, well...' He also notes the DMZ box may respond 'smoother and snappier (less hops)'. Crucially he doesn't claim to be right, he invites debate: 'So you tell me, DMZ or internal LAN? Why?'

*Bron: blogpost 'Citrix XenMobile MDM... To DMZ or not to DMZ? I might need your help one this one!' (2014-05-26), basvankaam.com.*

## Verwante notities

- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [Getting the XenMobile MDM server out of the DMZ was overdue and underdiscussed](mdm-out-of-dmz-relief.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
