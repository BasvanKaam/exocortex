---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [aws, snowball, edge-compute, ec2, data-transfer]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Snowball Edge: from data-transfer box to local compute

As of re:Invent 2018: AWS Snowball physical appliances move huge data volumes from on-prem to AWS when transferring over the internet would take too long. Snowball Edge added local compute (it can spin up EC2 instances to process data on-device before shipping it back). AWS then split it into Snowball Edge Storage Optimized (the original), Compute Optimized, and Compute Optimized with GPU. The compute options carried 42 TB S3-compatible storage plus 7.68 TB NVMe SSD, and could run instance combinations up to 52 vCPUs and 208 GiB memory. A durable underlying idea: bring cloud compute to where the data physically lives.

*Bron: blogpost '12 noteworthy announcements made during AWS re:Invent 2018' (2018-12-13), basvankaam.com.*

## Verwante notities

- [AWS EC2 (2006): birth of the commercial Cloud](aws-ec2-commercial-cloud-birth.md)
- [AWS Outposts: native AWS services in your own datacenter](aws-outposts-hybrid-native-services-on-prem.md)
- [AWS is still No. 1 in cloud, Microsoft is catching up fast](aws-still-number-one-microsoft-catching-up.md)
- [Storage tiering and lifecycle policies cut AWS storage cost](aws-storage-tiering-and-lifecycle-cost.md)
- [Azure data migration and import tools](azure-data-migration-import-tools.md)
