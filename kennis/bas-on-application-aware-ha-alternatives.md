---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [high-availability, vmware, fault-tolerance, symantec, sql, opinion]
layer: rich
bron: inside-citrix-fma
---

# Bas's take on application-aware HA alternatives for SQL

Beyond native SQL HA, Bas walks through four alternatives for protecting the Site database and gives his opinions:

1. VMware HA - great in itself but "simply is not application-oriented": it keeps the VM online if a physical host fails, but has no clue when the SQL database itself goes down (bad updates, full drives, stopped services). Same applies to Hyper-V and XenServer.
2. VMware App HA (Enterprise Plus) - more intelligent; can restart failed app components or reset the VM via the Application Awareness API without an OS reboot. Supports SQL, Tomcat, Apache, TC Server, IIS. Relatively complex (multiple VMs and management points), only supported on vSphere 5.5. For smaller/mid-sized companies already on VMware Enterprise Plus, this is "probably the most logical and cost-effective step."
3. VMware Fault Tolerance - "One of my favorites." As of vCenter/vSphere 6.0 a fault-tolerant machine can have up to 4 vCPUs (was one). Creates a live shadow instance always up to date with the primary; on hardware outage it triggers automatic failover with zero downtime and no data loss, then spins up a new secondary.
4. Symantec ApplicationHA - "probably the most Enterprise product of them all," though "not known by many." Supports over 23 tier 1 applications including custom/generic apps. Built on Symantec Cluster Server with Veritas agents; can restart app components, the OS, or the VM, and fall back to last known good backup. Manages via a vCenter plugin. A separate purchase needing a strong business case. Bas quotes a former colleague: "think big."

## Bron-citaten (NL, verbatim)

> VMware HA, and I guess the same goes for Hyper-V or XenServer as well, simply is not application-oriented.
>
> One of my favorites.
>
> think big, one of my former colleagues always used to say
