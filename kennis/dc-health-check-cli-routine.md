---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, domain-controller, troubleshooting, cli]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Domain Controller Health-Check CLI Routine

Bas's pre/post patch routine for a domain controller, piping each command to a text file so results are easy to read and search:

- `Dcdiag.exe /v` - tests the DC and its associated services; the must-run check for DC trouble.
- `Netdiag.exe /v` - checks networking components; the top of the log also confirms a patch really installed.
- `Netsh dhcp show server` - verifies DHCP server count and names (a server can silently lose authorization after a patch).
- `Repadmin /showreps` - shows replication and whether it succeeded (Global Catalogs show more here).
- `Repadmin /replsum /errorsonly` - surfaces who you are having replication issues with.

Always review the Event Viewer logs before and after, going back about a month for historical baseline.

*Bron: Core Knowledge doc 'Command - line Tooling Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Active Directory Command-Line Tools](active-directory-cli-tools.md)
- [AD FSMO Roles](ad-fsmo-roles.md)
- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [AD Sites and Replication Topology](ad-sites-and-replication-topology.md)
- [DNS and DHCP Command-Line Tools](dns-dhcp-cli-tools.md)
- [Never skip the basics: start troubleshooting at the event logs](never-skip-the-basics-event-logs.md)
- [Investigate, Analyse, Implement: Bas's structured troubleshooting approach](troubleshooting-investigate-analyse-implement.md)
