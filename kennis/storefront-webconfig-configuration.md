---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, storefront, web-config, webinterface, multi-site, powershell]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# StoreFront features configured via web.config

How it worked with StoreFront ~2.x (2014), as StoreFront replaced WebInterface (supported until June 2015):

- StoreFront added Receiver for Web, multi-site configurations (load balancing, HA, user mapping, subscription synchronisation, optimal NetScaler Gateway routing) and dropped the external database in favour of the built-in Windows Extensible Storage Engine.
- Many of these features are only configurable by editing the web.config file (analogous to the old WebInterface.conf), located at C:\inetpub\wwwroot\Citrix\<storename>\.
- Changes are effective on save; a misconfigured web.config simply breaks StoreFront.
- After editing web.config, some tasks become unavailable in the StoreFront GUI to prevent misconfiguration.
- In a StoreFront server group, edit web.config on only one server at a time, with the management console closed on the others; changes replicate automatically.
- PowerShell and the StoreFront management console cannot be open at the same time.
- Citrix released the separate StoreFront Web GUI Assistant to ease Receiver for Web configuration.

Examples requiring web.config edits: server-group subscription sync, optimal NetScaler Gateway routing, communication timeouts/retries, logon dialog, GSLB, default views, multiple domain lists, ICA file signing, desktop appliance sites.

*Bron: blogpost 'Installing and configuring Citrix StoreFront, the web.config file!' (2014-07-22), basvankaam.com.*

## Verwante notities

- [Critique: why isn't this in the GUI? (web.config friction)](build-it-into-the-gui-position.md)
- [StoreFront's powerful features shouldn't be locked behind web.config](storefront-config-should-be-in-the-gui.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [StoreFront over Web Interface, and StoreFront design notes](storefront-over-web-interface.md)
