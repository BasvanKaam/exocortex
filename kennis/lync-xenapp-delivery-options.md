---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [lync, xenapp, hdx, hsd, office-365]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Delivering Lync in a XenApp hosted shared desktop: generic vs optimized HDX

How it worked then (2015). To deliver Lync inside a XenApp hosted shared desktop you had two broad routes:

- Generic HDX: install the full Lync 2010 or 2013 client on the XenApp server. All audio/video processing happens server-side, which is heavy and the least preferred option.
- Optimized HDX: three options were available. The Lync VDI plug-in (offloads real processing to the endpoint device, saving VM resources), Local App Access (a.k.a. Reverse Seamless, introduced with XenDesktop 7.0), and the HDX RealTime Optimization Pack.

Key constraint for the customer case: the Lync VDI plug-in did not support Lync online (Office 365), only on-premises Lync infrastructures. So for a Lync online + XenApp HSD scenario, that optimized route was off the table regardless of whether it technically worked.

*Bron: blogpost 'Citrix XenApp & Microsoft (online) Lync... Things to be aware of. My findings!' (2015-03-29), basvankaam.com.*

## Verwante notities

- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [Citrix Summit 2015: Receiver X1, Framehawk, XenMobile 10](citrix-summit-2015-announcements.md)
- [HDX Browser Content Redirection renders client-side via CEF](hdx-browser-content-redirection-cef.md)
- [HDX extends ICA, it does not replace it](hdx-extends-ica-not-replaces.md)
- [Office 365 cached-mode OST files break on non-persistent desktops](office-365-ost-non-persistent-vdi-problem.md)
- [Don't make concessions on end user experience when delivering Lync](stance-lync-online-xenapp-concessions.md)
- [Teams in-browser video was gated to Edge user-agent (2019)](teams-browser-video-edge-gating-2019.md)
- [Citrix says supported, Microsoft says not: reading two support matrices at once](vendor-support-matrix-contradictions.md)
