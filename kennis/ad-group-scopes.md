---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, groups, global-catalog, reference]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# AD Group Scopes and Replication

The group scope model (still conceptually valid):

- **Domain local**: members from anywhere in the forest, trusted external forests, and trusted down-level domains; usable to grant resource permissions only within its own domain. Designed for use in DACLs on a domain's resources.
- **Global**: members only from its own domain, but can be granted permissions or nested in any trusting domain. Use to collect users/computers sharing a job or role.
- **Universal**: members from any domain in the forest; grantable permissions in any trusting domain, including other forests. Best for widely used groups that seldom change.

The canonical pattern (AGDLP): put accounts in global groups, nest those in domain local groups, assign permissions to the domain local group.

**Replication impact:** universal groups and all their members are listed in the global catalog, so any membership change replicates the entire membership to all GCs. Global and domain local groups appear in the GC but their members do not. Therefore use universal scope only where membership rarely changes; use global/domain local where it changes frequently to reduce GC size and replication traffic.

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Access Control: Security Descriptors, DACL, SACL](ad-access-control-descriptors.md)
- [AD FSMO Roles](ad-fsmo-roles.md)
- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [Active Directory Trust Types](ad-trust-types.md)
- [Share vs NTFS Permissions](share-vs-ntfs-permissions.md)
