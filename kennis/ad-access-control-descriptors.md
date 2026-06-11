---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, security, dacl, sacl, reference]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# AD Access Control: Security Descriptors, DACL, SACL

Access control in AD is administered per object by setting permissions (Full Control, Write, Read, etc.). Both shared objects and AD objects store permissions in **security descriptors**, which hold two access control lists:

- **DACL** (Discretionary ACL): identifies users/groups assigned or denied access. If a DACL does not explicitly grant a user (or a group they belong to), access is denied. Controlled by default by the object's owner; contains ACEs determining access.
- **SACL** (System ACL): identifies who to audit on successful or failed access, used to monitor security events and detect breaches.

**Inheritance:** by default objects inherit ACEs from their parent container's security descriptor, so access control defined at a container applies to subordinate objects — no need to reapply permissions on every child. Best practice: avoid changing default permissions or inheritance.

**User authentication and tokens:** the Local Security Authority (LSA) handles interactive auth (Kerberos or NTLM). Once identity is confirmed, the authenticating DC generates an access token containing the user's name, group memberships, the user's SID, and all group SIDs. Access control compares the SIDs in the token against the object's DACL — accounts are identified by SID, not name. Adding a user to a group after the token is issued requires logoff/logon to refresh the token. A Kerberos token can hold no more than 1,024 SIDs.

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Group Scopes and Replication](ad-group-scopes.md)
- [AD Naming: UPN, SAM and SPN](ad-naming-upn-spn.md)
- [Kerberos V5 Authentication](kerberos-v5-authentication.md)
- [How share and NTFS permissions combine](share-vs-ntfs-permission-combination.md)
- [Share vs NTFS Permissions](share-vs-ntfs-permissions.md)
