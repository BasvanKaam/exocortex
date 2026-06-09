---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [receiver, html5, clientless, storefront, account-discovery]
layer: reference
bron: inside-citrix-fma
---

# Three ways to reach resources via Receiver, including HTML5 clientless access

To view, subscribe to and launch resources you need a Citrix Receiver. When logging into a StoreFront web page (Receiver for Web), your system is checked for a supported Receiver; if absent you can download one from the page. Because installing Receiver isn't always possible, StoreFront also has a built-in HTML5 Receiver: 'clientless access', which also works as a fallback if a locally installed Receiver fails.

There are essentially three ways to reach resources (all involving Receiver in some form):
1. Receiver installed locally: provide your email address (when email-based account discovery is enabled), use a pre-configured provisioning file, or manually enter the StoreFront URL (supplied by IT). HTTPS is required.
2. Receiver for Web site: create a Store accessed via a browser; on logon your system is checked for a supported Receiver.
3. (Clientless) the built-in HTML5 Receiver.
