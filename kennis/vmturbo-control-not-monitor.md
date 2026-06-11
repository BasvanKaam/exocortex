---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vmturbo, monitoring, datacenter, capacity-planning]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VMTurbo: control the datacenter, don't just monitor it

How it worked then (2014): VMTurbo positioned itself not as another monitoring tool (Veeam, SolarWinds, vFoglight) but as a control system. It used "efficient market principles" to let workloads and infrastructure entities make their own resource-allocation decisions, dynamically adjusting the environment to meet application-specific SLAs.

Core product was Operations Manager, connecting to vCenter, SCOM, VCD or directly to hypervisors (VMware, Hyper-V, RHEV, Citrix), with plug-in modules on top. Deployed as a virtual appliance. They also offered a free Virtual Health Monitor.

The durable idea worth keeping: there is a meaningful distinction between monitoring (telling you something is wrong) and control (automatically keeping the system healthy). That framing outlived the product.

*Bron: blogpost 'Control, or control not. There is no manage! Free VMworld Europe tickets!' (2014-08-12), basvankaam.com.*

## Verwante notities

- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [HDX Monitor: HDX diagnostics tool](hdx-monitor-tool.md)
- [Linking infrastructure performance to employee productivity](infra-performance-vs-productivity.md)
- [After disruptive patches, measure impact per workload instead of guessing](measure-dont-guess-capacity-after-patches.md)
- [Reboots are a necessary evil; handle them proactively](proactive-over-reactive-ops.md)
- [Use health-check tooling proactively, not when things fall apart](use-health-checks-proactively-not-reactively.md)
- [Use health-check tooling proactively, not only when things fall apart](use-monitoring-proactively-not-when-it-breaks.md)
