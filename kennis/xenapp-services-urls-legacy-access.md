---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, xenapp-services-url, legacy, authentication, desktop-lock]
layer: reference
bron: inside-citrix-fma
---

# XenApp Services URLs for legacy Receiver access

Users who cannot upgrade to Citrix Receiver can still access StoreFront stores by configuring a XenApp Services URL on a per-store basis. This also works for domain-joined desktop appliances and repurposed PCs running the Citrix Desktop Lock. When you create a new store, the XenApp Services URL is enabled by default.

Drawbacks (from Citrix E-docs):
1. You cannot modify the XenApp Services URL for a store.
2. You cannot modify its settings by editing config.xml.
3. It supports explicit (default), domain pass-through, smart card, and pass-through-with-smart-card authentication. Only one authentication method per URL and one URL per store; multiple methods require separate stores.
4. Workspace control is enabled by default and cannot be configured or disabled.
5. Password-change requests are routed directly to the domain controller through the XenDesktop/XenApp/VDI-in-a-Box servers, bypassing the StoreFront authentication service.
