---
type: positie
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [positie, restore, testing, disaster-recovery, business-continuity, procedure, consulting-tool]
bron: salomon-opdrachten
---

# Restore Testing Cadence and Procedure

Bas's standing advice on validating a backup/restore solution: a backup you have never restored is not a proven backup. He builds an explicit testing cadence and a written procedure into the design rather than leaving restore as an assumed capability.

The recommendation pattern:

- **Monthly partial restore test.** At least once a month, restore a selection from the backup onto a separate environment and confirm the data and functionality come back. In practice this usually means restoring a domain controller and a database server plus one application server that leans on them - i.e. test the dependency chain, not a single file.
- **Periodic full restore.** At least over a multi-year horizon, perform a complete restore of every machine. Use that exercise to also test and improve the existing procedure.
- **A written restore procedure as a deliverable.** Beyond testing, document step-by-step how an operator actually performs a restore, with a short note per option and an included contact list (phone numbers per discipline). The same procedure doubles as the test script and can fold into the organization's on-call (piket) handbook. The real value of the procedure is removing any hesitation or open questions at the moment a restore is genuinely needed.

The generalizable position: design the restore *test* and the restore *runbook* as first-class deliverables, exercise them on a fixed cadence against the dependency chain, and treat "it restores" as something demonstrated, never assumed.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a public-safety / emergency-services organization (shared emergency control-room consolidation)).*

## Verwante notities

- [Design for Restore, Not Backup (RPO/RTO/MTPD First)](design-for-restore-not-backup.md)
- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [Fault-Tolerance Decision Hierarchy (Application HA Before Hypervisor HA)](fault-tolerance-decision-hierarchy.md)
- [Why high availability and DR matter: ransomware and data hostage](ransomware-data-hostage.md)
- [Windows Server Backup and VSS Block-Level Imaging](windows-server-backup-vss-block-level.md)
