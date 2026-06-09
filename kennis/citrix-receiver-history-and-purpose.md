---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-receiver, ica-client, merchandising-server, history, plugins]
layer: reference
bron: inside-citrix-fma
---

# Citrix Receiver: purpose and naming history

First introduced at Citrix Synergy in 2009, the Citrix Receiver was formerly known as the 'ICA Client'. The idea was (and is) that Receiver functions as a container or placeholder holding all other Citrix client software (ICA Client, Password Manager, SSL VPN client, Secure Access Gateway client, etc.), giving administrators a central point of management. The Receiver itself doesn't really do anything.

When Receiver was introduced, Citrix renamed existing clients (ICA Client to Online Plugin, Access Gateway client to Secure Access Plugin) and added an Offline Plugin and Web Plugin. These would 'plug in' to Receiver. To deliver and manage the plug-ins, Citrix introduced the Merchandising Server with Citrix Receiver 1.0, providing the admin interface to configure, deliver and upgrade plug-ins.

Receiver matured from version 1.0 (2009) to 4.4 (GA December 2015). Only as of version 3.0 was it actually a complete 'Citrix Receiver' package; before that it was a placeholder accompanied by the Merchandising Server. As of version 3.2, it moved away from the Merchandising Server toward Citrix.com for updates. 2018 update: the Workspace App will replace Receiver, again functioning as a placeholder for connectors and agents, plus doing much more.
