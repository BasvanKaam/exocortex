---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [windows-server-2008, backup, system-state, active-directory, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Windows Server 2008 System State Backup

Reference note on system state backup in Windows Server 2008.

A system state backup can only be performed from the WBADMIN.EXE command line; the MMC snap-in does not offer it:

wbadmin start systemstatebackup -backuptarget:e:

WBADMIN backs up the critical system files and application databases to a reserved system-state folder on the target. On a 32-bit Windows Server 2008 domain controller with a default DIT this ran a bit over 6GB, more than 5GB larger than on Windows Server 2003, partly because Windows Server Backup captures core OS files that NTBACKUP did not. Backup times grew accordingly, so plan for larger and slower system state backups when moving DCs to Windows Server 2008. WinRE is also built into the install process: booting from the install media exposes a Repair your computer option (easy to miss).

*Bron: Core Knowledge doc 'Windows Backup - VSS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD FSMO Roles](ad-fsmo-roles.md)
- [Domain Controller System State Recovery via DSRM](dc-system-state-recovery-dsrm-bcdedit.md)
- [Domain Controller System State Restore (DSRM)](dc-system-state-restore-dsrm.md)
- [Windows Server Backup to Network Shares: Limitations](windows-server-backup-network-share-limits.md)
- [Windows Server Backup and VSS Block-Level Imaging](windows-server-backup-vss-block-level.md)
