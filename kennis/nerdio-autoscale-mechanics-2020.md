---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-10
tags: [nerdio, wvd, autoscale, cost-optimization, host-pools]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain

Dynamic desktop pools scaled out/in on demand. Triggers in 2020: collective CPU usage, average active sessions, or available sessions (RAM usage was 'being worked on'). CPU was the default trigger.

Capacity controls: an upper host limit to cap cost, a lower limit for base capacity. 'Base host pool capacity' = hosts always part of the pool (stopped or active); 'min active host capacity' = minimum always running; 'burst beyond base capacity' = extra hosts spun up on above-average demand and the first to be removed on scale-in.

Graceful scale-in: when removing a host the system 'intelligently' picks the host with the fewest users, drains connections, and warns users first. The messaging setting let you notify users 5-60 minutes before drain (Bas noted a repeat-message mode would be handy). Pre-stage hosts could power on machines before a set time to beat boot storms.

Dated to the 2020 product, but the pattern (demand-based triggers + base/burst + graceful drain + pre-stage to beat boot storms) is durable autoscaling design for session-based desktops.

*Bron: blogpost 'How to: Nerdio Manager for WVD, first steps. Part two (host pools, autoscale, images)' (2020-04-16), basvankaam.com.*

## Verwante notities

- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [AVD Security Guidelines cheat sheet: a 35-item starting point](avd-security-cheat-sheet-starting-point.md)
- [Azure Ephemeral OS disks for stateless WVD workloads](azure-ephemeral-os-disks.md)
- [Ephemeral disks' biggest drawback disappears with the right autoscaler](ephemeral-disks-cons-as-pros.md)
- [Nerdio Manager for WVD roadmap as of mid-2020](nerdio-2020-product-roadmap-snapshot.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
- [Static vs dynamic host pools and autoscaling (Nerdio)](static-vs-dynamic-hostpools-nerdio.md)
- [The Azure calculator is fine, but MSPs need a real one](use-vendor-calculators-not-just-azure.md)
- [WVD Fall vs Spring release (non-ARM vs ARM)](wvd-fall-vs-spring-release.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
