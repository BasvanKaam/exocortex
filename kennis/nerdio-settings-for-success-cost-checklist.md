---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, cost-optimization, best-practice, autoscale]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# Settings for Success: Nerdio cost-optimization checklist

The closing best-practice set Bas teaches as the recurring cost-management discipline. The framing throughout: make incremental changes and monitor, don't set and forget.

1. Review auto-scaling savings monthly per host pool. Expect roughly 40-60% savings depending on usage; review history filtered by user sessions and savings graph.
2. Optimize auto-scale for hosts - are hosts sized right, too many/few sessions per host, best load-balancing option in place.
3. Review host sizing - is CPU/memory used predictably, are you under- or over-spec'd, is the environment cost-efficient.
4. Use FSLogix for a consistent UX; centrally manage multiple configs; simplify images by installing and hiding apps with app masking (built into Nerdio).
5. Review storage sizing for FSLogix - consider IOPS, throughput, latency; enable storage auto-scaling.
6. Tune the Log Analytics Workspace - set retention to requirements, consider user cost attribution and auto-shrink, adjust counters.
7. Enable auto-heal - define what a broken host is, configure reboots and recovery actions.
8. Use Reserved Instances, especially where always-on base capacity exists; model the impact and analyze per host pool.
9. Use Azure Capacity Extender (ACE) on host pools so Nerdio can provision alternative VM sizes when the default is unavailable; recommended by default unless you have specific requirements.
10. Use the VM Rightsizing service (VMRSS) - assesses demand over time for data-driven resize recommendations, works for personal and pooled.
11. Use the latest VM generation - moving Intel v4 to v5 can give up to ~24% better performance; a D16DS_v4 to v5 move saw ~12% more users per session host at near-identical cost.

dated:true because the specific savings percentages, VM generations and feature names are version/product-specific.

*Bron: Nerdio-content 'NEW_v3.0 Enterprise Training Camp_PRESENTER' (Training).*

## Verwante notities

- [AVD cost-component breakdown](avd-cost-component-breakdown.md)
- [NME first-admin RBAC and log analytics retention savings](nme-rbac-first-admin-and-savings.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
