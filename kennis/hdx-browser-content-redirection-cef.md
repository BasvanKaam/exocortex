---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, hdx, browser-content-redirection, cef, teams, vdi]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# HDX Browser Content Redirection renders client-side via CEF

How it worked in 2019 (Citrix Virtual Apps/Desktops 7.15 LTSR CU3). With Browser Content Redirection 2.0, the URL to display is passed from the VDA to the client via the Workspace App, and rendering happens locally on the client side using HdxBrowserCef.exe. That process does NOT use the locally installed Google Chrome; it embeds the open-source Chromium Embedded Framework (CEF) library, hence the 'Cef' in the executable name. Requires registry/policy keys to enable redirection plus the Browser Content Redirection Chrome extension. This is the same redirection model used for YouTube and, earlier, Flash redirection.

*Bron: blogpost 'Video calling using Microsoft Teams from a Citrix VDI environment - tricking Chrome' (2019-05-24), basvankaam.com.*

## Verwante notities

- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [Citrix HDX: an extension to ICA, not a replacement](citrix-hdx-extends-ica.md)
- [HDX extends ICA, it does not replace it](hdx-extends-ica-not-replaces.md)
- [Delivering Lync in a XenApp hosted shared desktop: generic vs optimized HDX](lync-xenapp-delivery-options.md)
- [Teams in-browser video was gated to Edge user-agent (2019)](teams-browser-video-edge-gating-2019.md)
- [ThinWire compatibility mode: the low-footprint fallback for H.264](thinwire-compatibility-mode.md)
