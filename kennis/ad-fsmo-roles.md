---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, fsmo, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# AD FSMO Roles

The five Flexible Single Master Operation roles:

**Forest-wide (1 per forest):**
- **Schema Master**: controls updates to the schema.
- **Domain Naming Master**: controls addition and removal of domains from the forest; lives in the root domain.

**Domain-wide (1 per domain):**
- **PDC Emulator**: backward compatibility for NT4 PDC operations (e.g. password changes), runs domain processes like the Security Descriptor Propagator (SDPROP), and is the master time server in the domain.
- **RID Master**: allocates pools of relative identifiers to DCs for creating objects.
- **Infrastructure Master**: synchronizes cross-domain group membership changes. Cannot run on a global catalog server unless all DCs are also GCs.

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Active Directory Command-Line Tools](active-directory-cli-tools.md)
- [AD Group Scopes and Replication](ad-group-scopes.md)
- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [AD Sites and Replication Topology](ad-sites-and-replication-topology.md)
- [Active Directory Trust Types](ad-trust-types.md)
- [Domain Controller Health-Check CLI Routine](dc-health-check-cli-routine.md)
- [Domain Controller System State Recovery via DSRM](dc-system-state-recovery-dsrm-bcdedit.md)
- [Windows Server 2008 System State Backup](windows-server-2008-system-state-backup.md)
