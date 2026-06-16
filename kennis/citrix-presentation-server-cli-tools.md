---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, presentation-server, cli, terminal-server]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix Presentation Server Command-Line Tools

Reference list of legacy Citrix Presentation Server / Terminal Server commands:

- **Data store / farm**: `DSCHECK` validates the data store (`/Clean` deletes inconsistent records - back up first); `DSMAINT` configures the data store DB; `DSVIEW` inspects data store / local host cache values; `CHFARM` moves a server to another farm.
- **Zone queries**: `QUERYDS` (local zone data collector), `QUERYDC` (find the data collector for a zone), `QFARM`/`Query Farm` (servers in an IMA farm), `Query server`, `Query license`.
- **Sessions**: `QUERY SESSION` / `Qwinsta`, `QUERY PROCESS` / `Qprocess`, `Quser`, `Reset winsta`, `Shadow` (shadow a session by name/ID, Ctrl+* to exit), `TSCON #` to take over a session.
- **Config**: `ICAPORT` (ICA TCP port), `CTXXMLSS` (move the Citrix XML Service off the IIS-shared port), `CLTPRINT` (client printer pipes), `TWConfig` (ICA display/graphics), `Change User /install|/execute` for installing apps.
- **Other**: `PRINTUI` (print driver/printer tasks), `AUDITLOG` (logon/logoff reports from the security event log).

*Bron: Core Knowledge doc 'Command - line Tooling Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Active Directory Command-Line Tools](active-directory-cli-tools.md)
- [Citrix Data Collector Elections](citrix-data-collector-elections.md)
- [Citrix IMA Architecture: Data Store and Local Host Cache](citrix-ima-architecture.md)
- [Citrix / Terminal Services logon sequence (reference)](citrix-ts-logon-sequence.md)
- [DNS and DHCP Command-Line Tools](dns-dhcp-cli-tools.md)
- [IMA-to-FMA terminology: Farm to Site, Data Collector to Delivery Controller](ima-to-fma-terminology-map.md)
