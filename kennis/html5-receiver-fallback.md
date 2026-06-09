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
