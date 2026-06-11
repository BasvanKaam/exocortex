---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [teams, browser, edge, user-agent, video-calling, chrome]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Teams in-browser video was gated to Edge user-agent (2019)

How it worked then. In 2019, Microsoft Teams in-browser video conferencing was server-side gated by browser: the backend checked the user-agent and only allowed Edge browsers to do video conferencing, even though Chromium technically had no blocker. The workaround Dennis Smith documented: spoof the user-agent to an Edge identifier so Teams permits video. Because HDX Browser Content Redirection rendered via CEF (not Chrome), the spoof had to be applied inside the Citrix Workspace App's libcef.dll, editing the user-agent string with a hex editor (strings terminate on &h00, space is &h20). Side effect: every redirected page, including YouTube, then requests as Edge. Explicitly a proof of concept, not recommended for production.

*Bron: blogpost 'Video calling using Microsoft Teams from a Citrix VDI environment - tricking Chrome' (2019-05-24), basvankaam.com.*

## Verwante notities

- [HDX Browser Content Redirection renders client-side via CEF](hdx-browser-content-redirection-cef.md)
- [Delivering Lync in a XenApp hosted shared desktop: generic vs optimized HDX](lync-xenapp-delivery-options.md)
