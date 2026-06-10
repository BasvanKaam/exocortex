---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-receiver, self-service-mode, web-access-mode, keywords, shortcuts]
layer: reference
bron: inside-citrix-fma
---

# Receiver Self Service Mode vs. Web Access Mode

Adding StoreFront to Receiver enables Self Service Mode (enabled by default): users subscribe to resources directly from the locally installed Receiver (right-click the system tray icon), and Keywords can pre-subscribe resources. An advantage over the more limited Web Access Mode (where Receiver isn't configured and users use a Receiver for Web site) is the ability to manage and customize the application shortcut location (Start menu and/or desktop) without users being able to uninstall. The two modes can be used side-by-side.

FMA fact: most of these shortcut-management options existed in Citrix Receiver Enterprise up to version 3.4, when it was killed; the functionality returned in Receiver 4.2.

Shortcut configuration examples (manual Receiver config):
- Self Service Mode lets users choose resources for their Start menu.
- Per-application settings can force specific resources onto desktops.
- PutShortcutsInStartMenu=False prevents auto-placing shortcuts in the Start menu.
- PutShortcutsOnDesktop=true places all shortcuts on the desktop.

FMA fact: disabling SelfServiceMode (enabled by default) means subscribed apps are only accessible via Start menu and desktop shortcuts, also called shortcut-only mode.

## Verwante notities

- [Bas's caution on pre-configured Start menus and desktops](bas-on-preconfigured-shortcuts-warning.md)
- [Bas's Citrix Receiver chapter key takeaways](receiver-chapter-key-takeaways.md)
- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
- [Self Service Store vs Mandatory Store and shortcut-only mode](self-service-vs-mandatory-store.md)
- [StoreFront resource subscription and Keywords](storefront-resource-subscription-keywords.md)
- [StoreFront subscriptions, Self Service Store and Keywords](storefront-subscriptions-and-keywords.md)
