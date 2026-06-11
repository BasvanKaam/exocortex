---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, rbac, administration, security]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenDesktop 7 delegated administration: roles, scopes, objects

How it worked then: XenDesktop 7 added custom administrator roles on top of the predefined ones (XD5 had only 5 fixed, non-customisable roles). The model rests on three concepts:
- Roles define what an admin can do (the permissions). Predefined roles were coarse: e.g. the Helpdesk Administrator could manage sessions/machines for ALL delivery groups with no way to limit which ones.
- Scopes define which specific objects (e.g. per department) the role applies to. A default scope named 'All' holds every Site object including future ones and cannot be deleted or modified; all predefined roles use it.
- Objects are the manageable items (desktops, catalogs, applications, hosts).

Workflow: create a custom role and assign high-level permissions plus sub-permissions (create/add/delete apps, add/remove machines, etc.); create a scope selecting the specific objects; then create an administrator and assign the role + scope to a domain user. Any domain user can be made an admin with no special prerequisites. Multiple custom profiles stack inclusively (permissions add up). A Resultant Set of Permissions tool showed effective permissions per admin account. Durable concept under the dated UI: scoped RBAC = role (what) x scope (on which objects).

*Bron: blogpost 'Delegated Administration... I'm just saying' (2013-10-14), basvankaam.com.*

## Verwante notities

- [Hiding apps (Limit Visibility) vs hiding desktops (PowerShell entitlement filter)](limit-visibility-vs-entitlement.md)
- [Positie: Citrix was inexplicably late adding delegated admin to XenDesktop](positie-citrix-late-with-xendesktop-delegated-admin.md)
