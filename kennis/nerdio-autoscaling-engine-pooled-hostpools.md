---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, wvd, avd, autoscale, host-pool, cost-optimization]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Nerdio autoscaling engine: pooled hostpool scaling logic

Detailed mechanics of the Nerdio Manager for WVD autoscale engine for pooled (hosted shared) desktops. Captured as durable explainer of the engine's knobs.

## Hostpool types
- **Static**: hosts added/removed manually via the GUI (no PowerShell).
- **Dynamic**: uses the autoscale engine, fully automated on preconfigurable scaling logic.

## Sizing controls
- **Base hostpool capacity**: minimum number of hosts in the pool at all times (these can be booted or shut down).
- **Min active host capacity**: how many of the base hosts must be active/booted at minimum. Can be 0 (100% savings) up to the full base count.
- **Active host defined as**: two states. "WVD Agent Available" (default) counts a host active only when the WVD back-end receives heartbeats and sees it Available. "VM Started" counts it active as long as the VM is running in Azure.
- **Burst beyond base capacity**: max extra hosts the engine may add (scale out) on top of the base capacity.

## Scale-out logic
- Default trigger is CPU usage. For GPU workloads (less CPU-sensitive) use **Available sessions** instead.
- Configure target available sessions across the pool and max sessions per host. When a host fills to its max sessions and no available session remains, the engine starts another host. Breadth-first load balancing distributes sessions evenly across hosts.

## Scale-in (the hard part)
Scaling in a hosted shared model is tricky because a host can carry multiple users. Controls:
- **Time restrictions**: only allow stop/scale-in within a window (e.g. 6 PM to 7 AM). Mind the time zone.
- **Scale-in aggressiveness** (after hosts are set to drain mode):
  - **High**: always scales in eventually except the Min active hosts. Empties session-less hosts first, then hosts with fewest active/disconnected sessions after notifying users. Biggest savings.
  - **Medium**: empties session-less hosts, then hosts with only disconnected sessions; never stops hosts with active sessions.
  - **Low**: only empties hosts with no sessions at all; UX gets top priority.

## Pre-staging (boot/login storm mitigation)
- Tell the engine to have N machines pre-booted by a target time (e.g. 2 machines ready at 8 AM). The engine calculates the lead time. Not a cost saving, a UX measure. Starting point: pre-stage 15-20% of total machine count and let autoscale handle the rest.

## Cost visibility
- Estimated Monthly Costs panel (Azure compute + storage only) updates live as you change VM type, OS disk, base capacity, or burst.
- Auto-scale history page shows exactly when/why machines powered on/off, with VM config, OS disk and region, and the amount saved versus running 24x7. Savings shown per tenant/workspace and per hostpool.

*Bron: Nerdio-content 'How to get the most out of your GPU enabled machines at the lowest cost possible, including a deeper dive into the Nerdio autoscaling engine' (Blogs).*

## Verwante notities

- [Autoscaling Can Beat Reserved Instances for Variable WVD Workloads](autoscaling-vs-reserved-instances-stance.md)
- [Azure GPU VMs: NVIDIA vs AMD NVv4, licensing and partitioning](azure-gpu-vms-licensing-and-nvv4-partitioning.md)
- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [Don't leave desktop power management to users alone](dont-leave-power-management-to-users.md)
- [Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling](ephemeral-disk-constraint-vs-autoscaling.md)
- [Nerdio Adoption & Management Framework: Five Foundational Elements](nerdio-adoption-management-framework.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Nerdio autoscaling for personal/persistent desktops](nerdio-autoscaling-personal-persistent-desktops.md)
- [Azure API limits and Nerdio's API Limit Booster](nerdio-azure-api-limit-booster.md)
- [Nerdio Manager storage autoscale for Azure Files Premium](nerdio-azure-files-premium-autoscale.md)
- [Nerdio Enterprise Optimization Journey (12-step framework)](nerdio-enterprise-optimization-journey.md)
- [How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)](nerdio-ephemeral-disks-jit-and-image-shrink.md)
- [Automating the Patch Tuesday image lifecycle in Nerdio](nerdio-patch-tuesday-image-lifecycle-method.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [NME persists machine names across reimage/rebuild](nme-hostpool-naming-persistence.md)
- [What the Nerdio autoscale engine does (NMW era)](nmw-autoscale-engine-capabilities.md)
- [Test GPU VMs, don't decide on price alone](test-dont-trust-pricing-on-gpu-vms.md)
