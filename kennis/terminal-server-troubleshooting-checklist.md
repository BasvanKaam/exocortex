---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [terminal-server, citrix, troubleshooting, active-directory, gpo, own-method]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Terminal Server / Citrix troubleshooting checklist (own notes)

Bas's own diagnostic checklist for user-facing Terminal Server / Citrix problems. The structure outlives the specific products: work from permissions outward to AD, GPO, scripts, and name resolution.

**Permissions**: rights on the folder, on the executable, on the database, and on service accounts (correct rights and passwords).

**Account and domain state**: was the user account deleted or disabled? Computer account reset, disabled, or deleted? Is the machine still a domain member? A deleted computer account can still have policies applying if replication has not completed.

**Replication and sites**: has replication between domain controllers happened yet? Multiple sites complicate this.

**Change history**: when did the problem first appear, what changed last, what software was installed, does everyone have it or only some users? Compare affected vs unaffected accounts, especially security groups, rights, GPOs, and logon scripts.

**AD placement**: is the user/computer account in the correct OU? Moving it can change which GPOs apply, useful as a test.

**GPOs and scripts**: are the right GPOs applied? Are settings coming from AD, from GPOs, or both (logon scripts, print scripts, home folders, TS profiles)? Where do drive mappings and home folders come from, AD or logon script, and could they conflict? Check drive letters.

**Name resolution**: did the IP change (check DHCP)? Was DNS changed, possibly not AD-integrated? Is an app reached by IP or by name (DNS)?

**Citrix specifics**: is the app launched via full Program Neighborhood or via an .ICA file? The web interface uses Default.ICA with a proxy address; full PN goes on IP or FQDN. Publish a test application via web interface and/or full PN to isolate.

**General**: check Event Viewer and the log of the relevant application or appliance (e.g. a Citrix CAG).

*Bron: Core Knowledge doc 'TS Steps' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix policy precedence: IMA vs Citrix AD vs normal AD policies](citrix-policy-precedence-ima-ad.md)
- [Citrix / Terminal Services logon sequence (reference)](citrix-ts-logon-sequence.md)
- [Never skip the basics: start troubleshooting at the event logs](never-skip-the-basics-event-logs.md)
- [Don't forget old-school tools (NetStat, Ping, Tracert, Telnet)](old-school-troubleshooting-tools.md)
- [PowerFuse assignment model and tracing (reference)](powerfuse-assignment-model-and-tracing.md)
- [How memory works in Terminal Server: shared executables](terminal-server-memory-shared-executables.md)
- [Terminal Server registry mapping and the load-balancing timestamp trap](terminal-server-registry-mapping-timestamp-trap.md)
- [Investigate, Analyse, Implement: Bas's structured troubleshooting approach](troubleshooting-investigate-analyse-implement.md)
