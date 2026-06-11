---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [stratusphere, monitoring, capacity-planning, opinion]
bron: basvankaam-blog
---

# After disruptive patches, measure impact per workload instead of guessing

Bas's recurring framing (Jan 2018, Meltdown/Spectre context): because the performance hit from the patches varies so much by CPU, socket type and workload that exact numbers are 'near to impossible' to predict, sizing infrastructure by guesswork is the wrong move ('this isn't the time to guess'). His position is to use real time-based in-guest and infrastructure metrics (he pitches Stratusphere UX) to see exactly which systems and applications are hit hardest, then resize or reorder hardware where actually needed, avoiding a 'needle in the haystack' approach. This 'measure, don't guess' stance recurs across his monitoring/EUC writing.

*Bron: blogpost 'Meltdown and Spectre - Minimize impact and avoid performance problems - how Stratusphere UX can help!' (2018-01-19), basvankaam.com.*

## Verwante notities

- [Use-cases for VDI/desktop benchmarking](benchmarking-use-cases.md)
- [Workspace/app lifecycle management is an unfairly neglected discipline](lifecycle-management-neglected-unfairly.md)
- [LTSR is the right call, but not for everybody](ltsr-is-not-for-everybody.md)
- [Measure to know (meten = weten)](measure-to-know-meten-is-weten.md)
- [Meltdown/Spectre patches carried a real performance cost - patch anyway](meltdown-spectre-patch-performance-cost.md)
- [Reboots are a necessary evil; handle them proactively](proactive-over-reactive-ops.md)
- [Processor Queue Length (PQL) as an early UX-degradation signal](processor-queue-length-as-ux-signal.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
- [Stratusphere UX is the Swiss Army knife of the portfolio](stratusphere-swiss-army-knife.md)
- [Stratusphere UX 6.1: dashboards, event log harvesting, process optimization](stratusphere-ux-61-features.md)
- [Use health-check tooling proactively, not only when things fall apart](use-monitoring-proactively-not-when-it-breaks.md)
- [VDI Drones: synthetic load testing without user accounts (2018)](vdi-drones-synthetic-load-testing.md)
- [VMTurbo: control the datacenter, don't just monitor it](vmturbo-control-not-monitor.md)
- [Windows 10 servicing branches and deployment rings](windows10-servicing-branches-rings.md)
- [Workspace/application lifecycle visibility uncovers waste and unmanaged machines](workspace-app-lifecycle-visibility-savings.md)
