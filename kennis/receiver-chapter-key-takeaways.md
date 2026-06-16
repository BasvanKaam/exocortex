---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [receiver, key-takeaways, self-service, sso, handshake]
layer: rich
bron: inside-citrix-fma
---

# Bas's Citrix Receiver chapter key takeaways

Bas's own summary list for the Receiver chapter:

- However you deploy Receiver, instruct your users and inform your helpdesk before configuration changes.
- Web Access and Self-Service modes are not mutually exclusive; they can run side-by-side.
- Self-Service mode was once a separate plugin; it is now built into Receiver. The most important modules making up Receiver today are the ICA Client software, the Self-Service plugin, and the Single Sign-on module for ICA.
- It all started with the ICA Client software (Bas dates this to 2009 in the takeaways), with many name changes and maturing technology since.
- The upcoming Receiver X1 is a great example of its evolution over the last decade.
- When upgrading Receiver, follow Citrix's step-by-step procedure (CTX135933). Receiver 4.4 should upgrade from any older version without issues. For pre-4.4 upgrade issues, use the Receiver Clean-Up utility (CTX137494).
- Remember the ICA handshake and virtual channels.
- Receiver can be configured via command-line, registry, StoreFront account settings, or per-application using Studio and GPOs.
- Not all features appear on the Receiver Feature Matrix.
- The HTML5-based built-in (StoreFront) Receiver is not enabled by default; enable it manually.

## Verwante notities

- [Bas's caution on pre-configured Start menus and desktops](bas-on-preconfigured-shortcuts-warning.md)
- [Citrix Receiver: purpose and naming history](citrix-receiver-history-and-purpose.md)
- [Receiver Clean-Up utility](receiver-cleanup-utility.md)
- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [Citrix Receiver / ICA Client detailed version timeline](receiver-detailed-version-timeline.md)
- [Receiver communications, ICA handshake and virtual channels](receiver-ica-handshake-and-virtual-channels.md)
- [Receiver platforms and the Receiver X1](receiver-platforms-and-x1.md)
- [Receiver Self Service Mode vs. Web Access Mode](receiver-self-service-vs-web-access-mode.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
