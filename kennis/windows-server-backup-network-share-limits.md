---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [windows-server-2008, backup, scheduling, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Windows Server Backup to Network Shares: Limitations

Reference note on the network-share constraints of Windows Server 2008 Backup.

Backing up to a network share works, but the tool cannot create a snapshot of the remote volume. So each full backup overwrites the previous one, leaving only the latest full image of each server on the share. Local and external disks can be set up on a daily backup schedule, but a network share cannot use the built-in backup scheduler (scheduled backups to a shared folder were only available on Windows Small Business Server code name Cougar).

Workaround: use the Windows Task Scheduler to run the WBADMIN command-line program for full backups to a network share, changing the target folder each time to avoid overwriting previous backups. Example command:

wbadmin start backup -backuptarget:\\backupserver\winbackup -include:c: -user:domein\backupaccount -password:MijnWachtwoord -quiet

The integrated scheduler is really designed for one thing: simple daily full-system backups to a local disk volume.

*Bron: Core Knowledge doc 'Windows Backup - VSS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Domain Controller System State Recovery via DSRM](dc-system-state-recovery-dsrm-bcdedit.md)
- [Windows Server 2008 System State Backup](windows-server-2008-system-state-backup.md)
- [Windows Server Backup and VSS Block-Level Imaging](windows-server-backup-vss-block-level.md)
