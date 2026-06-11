---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, trusts, forest, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Active Directory Trust Types

Reference for the trust types in Windows Server 2008-era AD:

- **External**: nontransitive, one-way or two-way. Access to resources in an NT 4.0 domain or a domain in a separate forest not joined by a forest trust.
- **Realm**: transitive or nontransitive, one-way or two-way. Trust between a non-Windows Kerberos realm and a Windows domain.
- **Forest**: transitive, one-way or two-way. Shares resources between forests; a two-way forest trust lets auth requests in either forest reach the other.
- **Shortcut**: transitive, one-way or two-way. Shortens logon times between two domains separated by two domain trees within one forest.

Transitive trusts are created automatically: each new domain gets a two-way transitive trust with its parent, and the trust path flows upward through the domain tree, so any account in the forest can authenticate at any domain in the forest.

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD FSMO Roles](ad-fsmo-roles.md)
- [AD Group Scopes and Replication](ad-group-scopes.md)
- [AD Naming: UPN, SAM and SPN](ad-naming-upn-spn.md)
- [Kerberos V5 Authentication](kerberos-v5-authentication.md)
