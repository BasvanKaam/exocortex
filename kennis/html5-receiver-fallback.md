---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [receiver, html5, storefront, launch-ica]
layer: reference
bron: inside-citrix-fma
---

# Receiver for HTML5 as a fallback

When you connect to StoreFront (directly or via NetScaler Gateway), it checks whether Receiver is installed locally and which OS you run; if not, it guides you to a download page (usually Citrix's).

If you can't or aren't allowed to install Receiver locally, Citrix offers the Receiver for HTML5, which connects to StoreFront/NetScaler and launches resources without loss of functionality. Disabled by default, StoreFront has a built-in HTML5 Receiver that activates at launch time by fetching the HTML5 engine from StoreFront and making it part of the local browser. You must use an HTML5-supported browser; the browser becomes your Receiver, handling the launch.ica file, and closing the browser closes the session. Even when Receiver is installed, the HTML5 Receiver can be enabled as a fallback mechanism.

## Verwante notities

- [Chromebooks valuable but not enterprise-ready (2014)](chromebooks-not-enterprise-ready-yet-2014.md)
- [Citrix dropped the Chromebook Receiver for HTML5](citrix-chromebook-receiver-to-html5.md)
- [Citrix Receiver: purpose and naming history](citrix-receiver-history-and-purpose.md)
- [Internal launch process: pooled VDI VM via StoreFront](internal-launch-process-pooled-vdi.md)
- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [Receiver communications, ICA handshake and virtual channels](receiver-ica-handshake-and-virtual-channels.md)
- [Receiver platforms and the Receiver X1](receiver-platforms-and-x1.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
