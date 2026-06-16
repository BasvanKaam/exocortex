---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmw, wvd, autoscale, cost, azure]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Nerdio Manager for WVD: the cost-saving levers (WVD era)

A durable map of how NMW reduces Azure Virtual Desktop spend. Product-specific and WVD-era (pre-AVD rename), so treat the mechanics as illustrative of the concepts rather than current UI.

## Autoscale (the headline lever)
- Non-persistent (multi-user/RDSH, pooled VDI): hosts are started, stopped, built from scratch, and fully removed by scaling logic. Logic can key on CPU usage, available sessions, or average active sessions.
- Scale-in aggressiveness (high/medium/low) governs which hosts the engine may remove: no/inactive sessions, disconnected sessions, or active sessions.
- Users get a configurable warning timer (up to an hour) before scale-in.
- VMs are put into drain mode before shutdown/removal.
- Pre-staging: have N hosts booted and ready on chosen weekdays/mornings to absorb login and boot storms.
- Specific hosts can be excluded from autoscale. All configurable per host pool.
- Persistent personal desktops (often GPU): start/stop fully automated once, never, or continuously, governed by power-off aggressiveness and pre-set working hours. Users can stop/start/restart/log off their own machines, and later change VM type or re-image.
- Claimed saving: up to 75% on WVD host compute and storage.

## Storage and disk levers
- Change disk type for stopped VMs (Premium SSD to Standard HDD) to cut storage cost while deallocated.
- Ephemeral OS disks: the OS disk is free but the VM cannot be deallocated, so you always pay compute unless the machine is destroyed each time. NMW turns this negative into a positive by being efficient at building/removing machines on a schedule.
- Auto-deallocate stopped-but-not-deallocated VMs via a periodic task (a common silent cost leak).
- Storage autoscale for Azure Files Premium: grow provisioned share size on anticipated demand or rising latency, shrink it when no longer needed (at most once per 24h). Premium file shares bill on provisioned size regardless of used capacity; IO and bandwidth limits scale with provisioned size.

## Scripted Actions (the automation primitive)
Simple but powerful: an internal library plus your own scripts. Anything PowerShell can start (Azure Runbooks, Bicep, JSON, Chocolatey) can run. Clone/alter existing scripts. Direct GitHub integration syncs a repo into NMW both ways. Actions can fire at many lifecycle points: image import, VM level, host pool level, machine create/start/stop/remove.

## Image management
Import from Shared Image Gallery, Azure custom images, Marketplace images. "Power off & set as image" automates the full Azure manual sequence: clone OS disk to a temp VM, remove local user accounts (so Sysprep doesn't fail on per-user modern apps), Sysprep /generalize, capture, swap in the new image, delete the temp VM. Re-image a host pool with control over parallelism, schedule/recurrence, and a user warning message with delay.

*Bron: Nerdio-content 'Costs savings' (Blogs).*

## Verwante notities

- [The real win of WVD automation is reclaimed admin time, not just compute](automation-saves-time-equals-money-position.md)
- [AVD cost-component breakdown](avd-cost-component-breakdown.md)
- [Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling](ephemeral-disk-constraint-vs-autoscaling.md)
- [Idea: NMW Blog/Content Backlog](idee-nmw-blog-backlog.md)
- [Nerdio Manager storage autoscale for Azure Files Premium](nerdio-azure-files-premium-autoscale.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Settings for Success: Nerdio cost-optimization checklist](nerdio-settings-for-success-cost-checklist.md)
- [What the Nerdio autoscale engine does (NMW era)](nmw-autoscale-engine-capabilities.md)
- [Hybrid WVD Object Model (NMW, Fall/Spring era)](nmw-hybrid-wvd-object-model.md)
- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
