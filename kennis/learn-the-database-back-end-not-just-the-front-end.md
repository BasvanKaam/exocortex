---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [sql, powershell, data, idee, positie]
layer: reference
gedateerd: nee
bron: salomon-it-blog
---

# Learn the database back-end, not just the front-end

Bas argues that consultants, admins and developers should learn to work with SQL and databases directly, instead of only consuming data through a front-end application. A front-end has already decided for you what is shown and how records relate; to go a step further you have to go back to the basics and look at, and adjust, the information yourself.

His reasoning: companies collect piles of data (customers, orders, devices, people). Once you learn SQL and adopt the accompanying way of thinking, you stop focusing on a single situation and start seeing the whole of the information.

Worked example he cites from practice: he had to find out which people worked in a specific hospital department. The hospital rented rooms to departments and the database recorded which devices were in which room and who was allowed to use them; querying that back-end let him derive who worked where and complete the project.

The second leg of the argument is PowerShell. SQL Server has shipped with a PowerShell add-on since 2008, which Microsoft offered precisely because tying the two together is valuable. With the database for configuration discovery (which machines need changing) plus PowerShell to execute the change, you can automate and speed up management work, provided you know how to handle both.

*Bron: Salomon-IT 'SBC Solutions - SQL en PowerShell technisch V2 - BvK' (Salomon Blogs).*

## Verwante notities

- [Cloud Cultural Shifts: DevOps, Automation, New Roles](cloud-cultural-shifts-overview.md)
- [How PowerShell DSC works: authoring, MOF, push and pull](desired-state-configuration-basics.md)
- [NetScaler Taskforce: a deeper training method than a 3-day course](netscaler-taskforce-deep-training-method.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [SQL Server 2008 Feature Highlights](sql-server-2008-feature-highlights.md)
- [Everything you do in Studio is PowerShell underneath](studio-is-powershell-underneath.md)
