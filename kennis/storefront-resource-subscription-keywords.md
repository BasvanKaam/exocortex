---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, subscription, keywords, resource-enumeration]
layer: reference
bron: inside-citrix-fma
---

# StoreFront resource subscription and Keywords

With StoreFront, users must first select and subscribe to resources (applications and/or desktops) from the store before they appear on the main home screen and can be launched. Using Keywords, administrators can pre-subscribe users to certain core resources so their home screen isn't completely empty on first login; this also works for assigned desktops. The syntax is to use the Keyword `auto` with the application and/or desktop of choice.

Resource enumeration kicks in right after a first-time user (no active/disconnected sessions) is authenticated, eventually showing the user their assigned resources. User authentication and resource enumeration basically go hand-in-hand.
