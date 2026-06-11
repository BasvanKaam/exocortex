---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, cli, ds-tools, administration]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Active Directory Command-Line Tools

The DS family and supporting tools for managing AD from the command line:

- **CSVDE** / **LDIFDE** - bulk import/export of directory data (CSV and LDIF format); LDIFDE can also extend the schema.
- **Dsadd / Dsmod / Dsrm / Dsmove** - add, modify, remove, and rename/move objects (users, groups, computers, contacts, OUs). Cross-domain moves use Movetree.
- **Dsquery / Dsget** - find objects by search criteria and display selected attributes.
- **Ntdsutil** - general AD database maintenance, single-master (FSMO) operations, and metadata cleanup for improperly removed DCs.
- **Netdom** - manage domains, trusts, and computer accounts; `netdom query fsmo` lists role holders.
- **Nltest** - test secure channels and verify trusts.
- **Repadmin** - inspect replication between DCs and sites.
- **Adprep** - extend the domain/forest schema.
- **Ldp.exe** - run raw LDAP searches against AD.

*Bron: Core Knowledge doc 'Command - line Tooling Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD FSMO Roles](ad-fsmo-roles.md)
- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [Domain Controller Health-Check CLI Routine](dc-health-check-cli-routine.md)
- [Domain Controller System State Restore (DSRM)](dc-system-state-restore-dsrm.md)
