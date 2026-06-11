---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [windows-server-2008, active-directory, recovery, dsrm, bcdedit, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Domain Controller System State Recovery via DSRM

Reference note on recovering Active Directory on Windows Server 2008.

For an Active Directory problem (for example recovering a deleted OU), restore the AD DS database to an earlier state rather than restoring the entire system. Even though AD DS can be stopped like a service in Windows Server 2008, you still must boot the server into Directory Services Restore Mode (DSRM) to perform a system state restore on a domain controller.

The boot environment was re-engineered for EFI, so the old boot.ini no longer exists; Windows Server 2008 uses Boot Configuration Data (BCD), managed with the BCDEDIT command-line tool. To reboot a DC into DSRM:

bcdedit /set safeboot dsrepair

*Bron: Core Knowledge doc 'Windows Backup - VSS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD FSMO Roles](ad-fsmo-roles.md)
- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [Domain Controller System State Restore (DSRM)](dc-system-state-restore-dsrm.md)
- [Windows Server 2008 System State Backup](windows-server-2008-system-state-backup.md)
- [Windows Server Backup to Network Shares: Limitations](windows-server-backup-network-share-limits.md)
- [Windows Server Backup and VSS Block-Level Imaging](windows-server-backup-vss-block-level.md)
