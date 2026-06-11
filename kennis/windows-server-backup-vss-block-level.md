---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [windows-server-2008, backup, vss, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Windows Server Backup and VSS Block-Level Imaging

Reference note on how Windows Server 2008 Backup worked.

It does block-level backups of the whole system and stores backup images in VHD format (compatible with Virtual Server), one VHD per backed-up volume, which you can browse. It is a feature that must be installed first. It backs up entire volumes, not selected files. The WBENGINE service does the heavy lifting whether you launch from the MMC snap-in or the command line.

Three ways it uses Volume Shadow Copy Service:
1. On a full backup it first makes a shadow copy of all source volumes, giving a consistent, lock-free view of the file system, then copies blocks to the target building a VHD per volume.
2. A snapshot gives a read-only copy so backup software reads every file without interfering with programs still writing to them.
3. It snapshots the source volume so VSS tracks changed blocks, enabling block-level incremental backups that only read the changed blocks.

Incremental behavior: the first backup copies all blocks to the VHD in compact but uncompressed form; later backups write only the changes, and old replaced data moves into the space reserved for shadow copies, with VSS computing the differences. The first backup is slow but subsequent ones are much faster. VSS snapshot benefits on the target only apply when backing up to a local hard disk.

*Bron: Core Knowledge doc 'Windows Backup - VSS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Copy-on-Write Snapshots vs Clones](copy-on-write-snapshots-vs-clones.md)
- [Domain Controller System State Recovery via DSRM](dc-system-state-recovery-dsrm-bcdedit.md)
- [Domain Controller System State Restore (DSRM)](dc-system-state-restore-dsrm.md)
- [Windows Server 2008 System State Backup](windows-server-2008-system-state-backup.md)
- [Windows Server Backup to Network Shares: Limitations](windows-server-backup-network-share-limits.md)
