---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [xenmobile, authentication, 2fa, mobility, citrix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenMobile PIN + certificate as two-factor auth

How it worked then (XenMobile 8.6): instead of typing complex AD passwords to launch apps, users could use a simple 4 or 5 digit PIN with SSO. The PIN worked together with a digital certificate installed on the device that held the user's AD credentials, so the PIN acted as a second factor complementing the certificate.

Key security property: if the device is lost or someone leaves, IT deletes the certificate remotely and the device becomes useless for corporate access even if the PIN is known, since the PIN does nothing without the certificate. Selective or full remote wipe are the additional options.

*Bron: blogpost 'Citrix XenMobile (8.6) revisited' (2013-11-02), basvankaam.com.*
