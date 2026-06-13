---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-10
tags: [ephemeral-disks, autoscaling, WVD, Nerdio, opinion]
bron: basvankaam-blog
---

# Ephemeral disks' biggest drawback disappears with the right autoscaler

Bas's framing (July 2020): the main objection to Ephemeral disks, that the VM can't be stopped/deallocated, only restarted, is neutralised by an autoscaler that adds and removes VMs while retaining machine name, IP, DNS and AD records. Nerdio's autoscaling does exactly this, so it can drop to 0 active machines for optimal cost control. Combined with the disks being free and 50-70% faster to boot, he calls it a 'win-win-win'. This is a clear product-advocacy take: position a generic Azure limitation as a non-issue specifically because Nerdio's mechanism handles it (added in Nerdio Manager for WVD 2.1.0).

*Bron: blogpost 'What are Azure Ephemeral disks, how to use them with WVD, and why care?' (2020-07-01), basvankaam.com.*

## Verwante notities

- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [Azure Ephemeral OS disks for stateless WVD workloads](azure-ephemeral-os-disks.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [Ephemeral OS Disks are underrated for stateless AVD](positie-ephemeral-os-disks-underrated.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
