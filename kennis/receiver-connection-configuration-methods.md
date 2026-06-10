---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-receiver, email-based-discovery, provisioning-file, storefront, dns]
layer: reference
bron: inside-citrix-fma
---

# Configuring Receiver connection information

Three ways to tell Receiver how and where to connect:

1. Email-based account discovery (popular): users fill in their email address; Receiver automatically determines the associated NetScaler Gateway or StoreFront server using DNS Service (SRV) records, then prompts for domain credentials. FMA fact: email-based discovery requires StoreFront; it does not work with Web Interface.
2. Provisioning files: created with StoreFront, containing connection details. Users double-click the file and Receiver is automatically configured. The provisioning file (and the Receiver installer) can also be offered on Receiver for Web sites.
3. Manual entry: provide users the StoreFront server address (or a XenApp Services site if still on 6.5) to enter themselves. Receiver verifies the connection, then prompts for credentials.

## Verwante notities

- [Beacon-based Receiver connection routing](beacon-based-receiver-connection-routing.md)
- [Citrix Receiver: purpose and naming history](citrix-receiver-history-and-purpose.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [Receiver for HTML5 as a fallback](html5-receiver-fallback.md)
- [Bas's Citrix Receiver chapter key takeaways](receiver-chapter-key-takeaways.md)
- [Receiver Clean-Up utility](receiver-cleanup-utility.md)
- [Receiver Self Service Mode vs. Web Access Mode](receiver-self-service-vs-web-access-mode.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
- [Bas's StoreFront chapter key takeaways](storefront-chapter-key-takeaways.md)
- [StoreFront over Web Interface, and StoreFront design notes](storefront-over-web-interface.md)
- [StoreFront vs Web Interface user authentication](storefront-vs-web-interface-authentication.md)
- [XenApp Services URLs for legacy Receiver access](xenapp-services-urls-legacy-access.md)
