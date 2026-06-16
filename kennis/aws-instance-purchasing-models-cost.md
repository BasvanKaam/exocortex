---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [aws, ec2, reserved-instances, spot-instances, scheduled-instances, cost-savings]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Reserved, Scheduled and Spot instances as AWS cost levers

From Bas's 30-tips AWS cost guide (Jan 2019): beyond on-demand pricing, the main EC2 purchasing levers are Reserved Instances (commit for a term in exchange for a discount), Scheduled Instances (reserve capacity for recurring time windows), and Spot Instances (bid on spare capacity for the biggest savings, with the trade-off that they can be reclaimed). He also flags optimization aids like the Spotinst Elastigroup platform, ARM-based EC2 instances (Linux only at the time) and EC2 hibernation. The durable concept: match the purchasing model to the workload's predictability and interruptibility to cut compute cost; the specific products/limits are 2019-era.

*Bron: blogpost 'THIRTY AWS Pro TIPS on how to use the Cloud more efficiently and save some money' (2019-01-16), basvankaam.com.*

## Verwante notities

- [How AWS AppStream 2.0 streams apps (2019)](appstream-fleets-image-builder.md)
- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [AWS native cost-management toolset (TCO, Budgets, Cost Explorer, Trusted Advisor)](aws-native-cost-management-tools.md)
- [Storage tiering and lifecycle policies cut AWS storage cost](aws-storage-tiering-and-lifecycle-cost.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [Cloud cost-optimization levers](cloud-cost-optimization-levers.md)
- [EC2 hibernation preserves in-memory state to save compute cost](ec2-hibernation-saves-compute-cost.md)
- [Reserved Instances: 12% early-exit fine and monthly payment](reserved-instance-early-exit-fine.md)
