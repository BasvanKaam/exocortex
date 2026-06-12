---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [wvd, azure, costs, fslogix, lab, deallocation]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Cheap WVD lab: de-allocate VMs, pay only for storage

Durable Azure cost principle, illustrated with a 2019 WVD preview lab. Bas ran a minimal lab: one IaaS Domain Controller (also serving as file server, since WVD needs some form of AD) plus a single Windows 10 VM (Standard A2 v2, 2 vCPU, 4 GiB) provisioned from the standard template with FSLogix built in. Two VMs, two disks, two NICs, one each of Availability Set, Resource Group, VNet, NSG, Storage Account, Public IP.

The cost lever: most of the time the VMs are shut down, stopped and de-allocated, so compute costs nothing; you only pay for the storage (the disks). Spin them up manually when needed. Over two months of occasional use (a few hours at most, plus several demos), total was about 12-13 dollars, almost entirely storage. The durable lesson outlasts WVD preview: in Azure, a stopped-but-not-deallocated VM still bills compute; de-allocating is what stops the meter.

*Bron: blogpost 'A short one on monthly costs associated with WVD in preview' (2019-07-15), basvankaam.com.*

## Verwante notities

- [Azure cost-control habits for a test lab](azure-classic-cost-control-takeaways.md)
- [Azure Ephemeral OS disks for stateless WVD workloads](azure-ephemeral-os-disks.md)
- [Moving to the cloud does not automatically save money](cloud-does-not-automatically-save-money.md)
- [CloudJumper optimization features, platform VM, and pricing (2019)](cloudjumper-optimization-features-and-pricing-2019.md)
- [EC2 hibernation preserves in-memory state to save compute cost](ec2-hibernation-saves-compute-cost.md)
- [Ephemeral disks' biggest drawback disappears with the right autoscaler](ephemeral-disks-cons-as-pros.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [Reserved Instances: 12% early-exit fine and monthly payment](reserved-instance-early-exit-fine.md)
- [WVD will only get easier and cheaper, lowering the barrier](wvd-lowering-the-barrier-prediction.md)
- [WVD preview constraints (2019)](wvd-preview-good-to-knows.md)
