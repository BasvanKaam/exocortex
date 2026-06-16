---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [aws, s3, glacier, efs, tiering, lifecycle, cost-savings]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Storage tiering and lifecycle policies cut AWS storage cost

Storage cost-saving patterns from the 2019 AWS guide: S3 Intelligent-Tiering and S3 lifecycle policies move data to cheaper tiers automatically based on access patterns; Glacier provides low-cost archival storage for rarely accessed data; EFS Infrequent Access (Linux only) lowers file-storage cost; and S3 can be used without an EC2 instance for some use cases. The durable principle: classify data by access frequency and let tiering/lifecycle rules push cold data to cheaper storage rather than paying hot-tier rates for everything.

*Bron: blogpost 'THIRTY AWS Pro TIPS on how to use the Cloud more efficiently and save some money' (2019-01-16), basvankaam.com.*

## Verwante notities

- [AWS cost management and optimisation tools](aws-cost-management-tools.md)
- [Reserved, Scheduled and Spot instances as AWS cost levers](aws-instance-purchasing-models-cost.md)
- [AWS native cost-management toolset (TCO, Budgets, Cost Explorer, Trusted Advisor)](aws-native-cost-management-tools.md)
- [Snowball Edge: from data-transfer box to local compute](aws-snowball-edge-compute-variants.md)
- [Azure Files: a cloud NAS, plus Azure File Sync for hybrid](azure-files-cloud-nas.md)
- [Cloud cost-optimization levers](cloud-cost-optimization-levers.md)
- [EC2 hibernation preserves in-memory state to save compute cost](ec2-hibernation-saves-compute-cost.md)
