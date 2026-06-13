---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio-manager, azure-files, fslogix, autoscale, storage, avd]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Nerdio Manager storage autoscale for Azure Files Premium

The core problem Nerdio's storage autoscale solves: Azure Files **Premium** uses the *provisioned model*. You pay for all provisioned capacity even when unused, with a 100 GB default minimum. Provisioning "just to be sure" (e.g. 1 TB while only 30-40% is in use) means the billing meter runs from day one on storage you don't yet need. Standard tier is pay-as-you-go but lacks the performance FSLogix needs. Reserved Capacity (1 or 3 year) lowers cost but still locks you into a guessed-at provisioned amount.

Nerdio Manager's autoscale engine makes Premium behave close to pay-as-you-go:
- Start at the 100 GB Premium minimum; the engine **grows** the provisioned share size in response to anticipated demand or rising latency, and **shrinks** it again when the headroom is no longer needed (no more than once every 24 hours, a limit inherited from how the native Azure Files service works).
- Growth increments are configurable to any value (10, 20, 50, 100 GB, etc.), continuing up to the Azure Files maximum or your own set ceiling. Quota units can be set in GB or in %.
- Latency-driven scaling: it monitors request latency in ms and scales out/in on thresholds, e.g. exceed 15 ms for 5+ minutes -> scale out 100 GB; drop below 10 ms for 5+ minutes -> scale down 100 GB. Trigger can be the average or maximum time to process a successful request.
- Because Premium performance characteristics grow with provisioned GB, this is effectively scaling on **performance** as well as capacity; the config page shows the resulting performance characteristics in real time as you edit metrics.
- Schedule-based scaling: pre-provision extra capacity/performance on specific weekdays or weekends, scale down when no longer needed.

Rule of thumb sizing context: FSLogix Profile Containers average ~5-20 GB in the field (use ~15 GB as a planning average), so even small environments cross the 100 GB Premium minimum quickly. Bas's field observation: roughly 75% of customers he talks to use Azure Files this way for AVD profiles.

*Bron: Nerdio-content 'Azure Files' (Blogs).*

## Verwante notities

- [Five (plus RI) AVD cost-reduction options](avd-five-cost-reduction-options.md)
- [Azure Files tiers and pricing model (reference)](azure-files-tiers-reference.md)
- [IOPS, latency, and sizing storage for VDI workloads](iops-latency-and-sizing-storage-for-vdi.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
- [Reserved Capacity still leaves you guessing; autoscale is the better answer](position-reserved-capacity-vs-autoscale.md)
