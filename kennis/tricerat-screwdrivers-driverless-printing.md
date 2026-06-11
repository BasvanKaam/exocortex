---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, citrix, tricerat, screwdrivers, rdsh, vdi]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Driverless printing in Citrix/VDI: ScrewDrivers and Simplify Printing

How it worked then (Tricerat, 2018): printing in Citrix/RDSH/VDI is notoriously painful because of native print-driver management. Tricerat ScrewDrivers (introduced 2001) removes the need to install any print drivers except its own. A server component and a client plugin work over RDP/ICA/PCoIP virtual channels; when you print, a virtual printer is created server-side, the job is compressed using Tricerat's TMF protocol and streamed to the client, which prints to the real (direct-attached or network) printer. It preserves features like secure/PIN print, stapling, collating and duplexing.

Simplify Printing extends this: no print driver on the RDSH/VDI machine or client at all, yet full native-driver feature access. A Simplify Suite component on the session host and a Print Server Agent on the print server talk over TCP/IP, a SQL database stores which printers a user gets and mirrors native drivers from the print server. ScrewDrivers and Simplify can be mixed. The general universal-print-driver caveat still applies: a single universal driver is simplest but historically falls short for advanced native features.

*Bron: blogpost 'Focus on Citrix (or VMware, or Microsoft) - not printing!' (2018-02-21), basvankaam.com.*

## Verwante notities

- [Citrix printing barely changed across 2018 releases](citrix-printing-stagnation-2018.md)
- [Printing is the perennial pain admins shouldn't have to focus on](printing-is-a-perennial-euc-pain.md)
