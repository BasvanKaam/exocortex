---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, subscriptions, keywords, self-service-store, receiver]
layer: reference
bron: inside-citrix-fma
---

# StoreFront subscriptions, Self Service Store and Keywords

By default with StoreFront (Receiver for Web with an unconfigured Receiver), users must subscribe to resources before they appear on their home screen, so authentication and enumeration go hand in hand. This default is called the 'Self Service Store' and can be disabled from the GUI.

Admins can pre-subscribe users to core apps using Keywords (configured in Studio on the application's details), prepopulating home screens at first login; this also works for assigned desktops. The Keyword 'AUTO' makes a resource appear automatically. Multiple Keywords can be combined; others include PREFER, FEATURED, PRIMARY, MANDATORY. (Bas references Martijn Hulsman's article on StoreFront Keywords.)

FMA facts: besides Receiver for Web, you can configure Citrix Receiver in self-service mode so users subscribe directly from the local Receiver interface. As of Citrix Receiver 4.2.100 you can also integrate app/desktop shortcuts into users' Start menus or desktops with no subscription needed.

## Verwante notities

- [Bas's caution on pre-configured Start menus and desktops](bas-on-preconfigured-shortcuts-warning.md)
- [Receiver Self Service Mode vs. Web Access Mode](receiver-self-service-vs-web-access-mode.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
- [Self Service Store vs Mandatory Store and shortcut-only mode](self-service-vs-mandatory-store.md)
- [Bas's StoreFront chapter key takeaways](storefront-chapter-key-takeaways.md)
- [StoreFront resource subscription and Keywords](storefront-resource-subscription-keywords.md)
- [StoreFront subscription storage, server groups and synchronization](storefront-subscription-storage-and-sync.md)
