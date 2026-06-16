---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [aws, ec2, hibernation, ebs, cost-savings]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# EC2 hibernation preserves in-memory state to save compute cost

Introduced at re:Invent 2018: hibernation for certain EC2 instances writes the machine's in-memory state to a file on the root EBS volume before shutting down, so you skip the cost of a fresh boot/config while paying no compute charges during hibernation. At launch it covered Amazon Linux 1 on M3/M4/M5, C3/C4/C5, R3/R4/R5 instances; Linux 2 support was in progress and Windows was not yet supported. The durable concept: pause a workload cheaply while keeping its warm state for fast resume.

*Bron: blogpost '12 noteworthy announcements made during AWS re:Invent 2018' (2018-12-13), basvankaam.com.*

## Verwante notities

- [Reserved, Scheduled and Spot instances as AWS cost levers](aws-instance-purchasing-models-cost.md)
- [AWS native cost-management toolset (TCO, Budgets, Cost Explorer, Trusted Advisor)](aws-native-cost-management-tools.md)
- [Storage tiering and lifecycle policies cut AWS storage cost](aws-storage-tiering-and-lifecycle-cost.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
