---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [html5, vdi, rdsh, browser-client, awingu]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# HTML5 browser clients: appeal and historical pain points

How it worked around 2020: the pitch for HTML5-based VDI/RDSH clients was that any device with a browser could connect via just a URL, with no client install, no software updates, and no VPN. The rest is built into the browser. This lowered the barrier for novice users working from home.

The historically hard problems for these clients (not unique to HTML5) were multi-monitor support, printing, and smartcard support. Awingu 4.3 addressed these: a Display Manager supporting up to 16 screens (the RDP limit), a virtual printer needing no print drivers (or use of office network printers), and smartcard support via an in-house Remote Application Helper. The architecture was an HTML5 gateway fronting RDP back-ends (RemoteApp, Remote Desktop, VDI) over SSL.

Durable takeaway underneath the dated product specifics: when evaluating a browser-only access layer, the make-or-break features are multi-monitor, printing, and smartcard/peripheral support, because those are where the browser-only model historically breaks.

*Bron: blogpost 'HTML5 Browser Clients and Awingu' (2020-03-17), basvankaam.com.*

## Verwante notities

- [Awingu as an HTML5 workspace aggregator](awingu-html5-workspace-aggregator.md)
- [The browser as the aggregation layer / new OS](browser-as-the-new-os.md)
- [Chromebooks require an online state of mind](chromebook-online-state-of-mind.md)
- [Chromebooks valuable but not enterprise-ready (2014)](chromebooks-not-enterprise-ready-yet-2014.md)
- [Citrix dropped the Chromebook Receiver for HTML5](citrix-chromebook-receiver-to-html5.md)
- [Printing is the perennial pain admins shouldn't have to focus on](printing-is-a-perennial-euc-pain.md)
- [WFH is not going away anytime soon](wfh-is-here-to-stay-2020.md)
- [WVD will only get easier and cheaper, lowering the barrier](wvd-lowering-the-barrier-prediction.md)
