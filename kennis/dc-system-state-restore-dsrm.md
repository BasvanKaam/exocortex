---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, backup, dsrm, bcdedit, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Domain Controller System State Restore (DSRM)

How AD recovery worked on Windows Server 2008. To recover from an AD problem (e.g. restoring a deleted OU), restore the AD DS database to an earlier state rather than the whole system. Even though AD DS can be stopped like a service in Server 2008, a system state restore on a DC still requires booting into **Directory Services Restore Mode (DSRM)**.

Server 2008 re-engineered the boot environment for EFI: the old boot.ini is gone, replaced by Boot Configuration Data (BCD), managed with the BCDEDIT command-line tool. To reboot a DC into DSRM:

```
bcdedit /set safeboot dsrepair
```

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Active Directory Command-Line Tools](active-directory-cli-tools.md)
- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [Domain Controller System State Recovery via DSRM](dc-system-state-recovery-dsrm-bcdedit.md)
- [Windows Server 2008 System State Backup](windows-server-2008-system-state-backup.md)
- [Windows Server Backup and VSS Block-Level Imaging](windows-server-backup-vss-block-level.md)
