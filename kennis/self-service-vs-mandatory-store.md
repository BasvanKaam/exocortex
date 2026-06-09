---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, receiver, self-service, keywords]
layer: reference
bron: inside-citrix-fma
---

# Self Service Store vs Mandatory Store and shortcut-only mode

StoreFront defaults to the 'Self Service Store' setup, where users subscribe themselves to resources they are permitted to start. Disabling it leaves the 'Mandatory Store' configuration, where all permitted resources display by default with no subscription needed.

Keywords (configured in Citrix Studio) can auto-subscribe users to certain resources (e.g. a standard desktop) so they appear directly on the welcome screen. As of Citrix Receiver 4.2.100, application and desktop shortcuts can also be integrated into Start menus or placed on desktops with no subscription needed.

Disabling SelfServiceMode (enabled by default) means subscribed apps are only reachable via Start menu and desktop shortcuts — known as shortcut-only mode.
