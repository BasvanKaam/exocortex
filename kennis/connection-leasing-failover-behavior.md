---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [connection-leasing, failover, limitations, registry, gpo]
layer: reference
bron: inside-citrix-fma
---

# Connection Leasing failover behavior and limitations

Connection Leasing only becomes active when none of the active Delivery Controllers can reach the Central database. When it kicks in, by default there is a two-minute period where no connections are brokered (to allow SQL HA to fail over); then locally cached leases become active. Registered VDAs deregister and re-register once the database returns.

Active leasing uses the Launch files to launch resources by contacting the machine where the resource was last successfully started. Lease information is valid for a maximum of two weeks (14 days) by default, configurable via Registry or GPO:
- GPO: HKLM\Software\Policies\Citrix\DesktopServer\ConnectionLeasing
- Registry: HKLM\Software\Citrix\DesktopServer\ConnectionLeasing

Limitations while Connection Leasing is active:
- Desktop Studio and Director operations are unavailable.
- PowerShell cmdlets requiring database access don't work.
- No VDA load balancing occurs.
- Users can only connect to the last host they connected to.
- A 2-minute brokering gap exists when the database becomes unavailable or is restored.
- Users must have logged on within the default 14-day period.
- Connection Leasing only works for assigned resources, not pooled desktops, and does not support anonymous users.

## Verwante notities

- [The Central Site database in the FMA](central-site-database-fma.md)
- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [Connection Leasing is not Local Host Cache, and it's not HA](cl-is-not-lhc-and-not-ha.md)
- [How Connection Leasing worked in XenApp 7.6](connection-leasing-how-it-works.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [FMA Local Host Cache: Principal Broker, Secondary Broker (HA) and CSS](fma-local-host-cache-services.md)
- [IMA Zones vs. FMA Zones comparison](ima-zones-vs-fma-zones-comparison.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
