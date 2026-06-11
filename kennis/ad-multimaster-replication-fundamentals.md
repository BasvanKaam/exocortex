---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, replication, usn, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Active Directory Multimaster Replication

How AD replication worked in the Windows 2000/2003 era. AD uses multimaster replication: a DC that takes a change notifies its replication partners. After a stable change, the source DC waits before notifying (5 minutes / 300 seconds in Windows 2000, 15 seconds in Windows 2003), and only notifies one partner every 30 seconds so it is not overwhelmed with update requests.

Partners send an update request carrying a USN (Update Sequence Number) back to the DC that made the change. Each change has a unique USN, so the source DC knows the requesting DC's state and sends only the deltas. Each updated DC in turn notifies its own partners. Absent any change, a DC still replicates every 6 hours by default.

Urgent replication (e.g. account lockouts, password changes pushed to the PDC) replicates immediately rather than waiting.

Transport: intrasite replication always uses RPC over IP (required to support FRS). SMTP may be used for replication between sites.

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Active Directory Command-Line Tools](active-directory-cli-tools.md)
- [AD FSMO Roles](ad-fsmo-roles.md)
- [AD Group Scopes and Replication](ad-group-scopes.md)
- [AD Sites and Replication Topology](ad-sites-and-replication-topology.md)
- [Domain Controller Health-Check CLI Routine](dc-health-check-cli-routine.md)
- [Domain Controller System State Recovery via DSRM](dc-system-state-recovery-dsrm-bcdedit.md)
- [Domain Controller System State Restore (DSRM)](dc-system-state-restore-dsrm.md)
- [DNS zone transfer and Notify](dns-zone-transfer-and-notify.md)
- [DNS zone types](dns-zone-types.md)
- [Synchronous vs Asynchronous Replication](synchronous-vs-asynchronous-replication.md)
