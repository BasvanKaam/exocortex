---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, data-collector, elections, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix Data Collector Elections

A Data Collector is a regular Presentation Server whose IMA service has also taken on that role; it is **elected**, not picked, because a DC must always exist for consoles and user connections to work.

Election mechanics: when a PS's IMA service starts, it contacts other servers (IMA protocol, port 2512) until it finds one online, learns which server is the current DC, and challenges it. The winner is whichever server runs the newest version of the IMA service — a newer CPS version, a feature pack, or relevant hotfixes can win (only hotfixes touching the IMA service affect the outcome). So you control the DC by keeping the desired server the most up to date.

The console election-preference settings (most preferred / preferred / default / not preferred) are tiebreakers only, used when multiple servers have identical versions and hotfixes; they are ignored when a newer server is up for election.

Elections occur when: the IMA service starts on any server; a PS fails to contact the DC; the current DC goes offline (gracefully it sends an election request first); a new server comes online; a zone's configuration changes (server added/removed or new zone); or one DC unexpectedly finds another DC. After a new DC is elected, the other servers send it their current session data to populate its dynamic store; if the DC is unchanged, they do not resend.

*Bron: Core Knowledge doc 'Citrix General Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix IMA Architecture: Data Store and Local Host Cache](citrix-ima-architecture.md)
- [Citrix Presentation Server Command-Line Tools](citrix-presentation-server-cli-tools.md)
- [Citrix Server, Farm and Zone Design Trade-offs](citrix-server-farm-zone-design.md)
- [Citrix Zones and Data Collectors](citrix-zones-and-data-collectors.md)
- [Cluster Quorum Models](cluster-quorum-models.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
