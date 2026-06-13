---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [azure-files, storage, fslogix, smb, reference]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Azure Files tiers and pricing model (reference)

Quick durable reference Bas uses when designing AVD/FSLogix storage. (Mostly known; kept for the tier-naming and billing-model distinctions that trip people up.)

- Azure Files = fully managed SMB/NFS file shares, serverless, replacing IaaS file-server VMs or NAS. Built on storage accounts (top-level pools that also hold blob/queue/table).
- **Standard tier** was renamed **Transaction Optimized** (HDD-backed). Microsoft added two cheaper HDD options to this family: **Hot** (general-purpose team shares) and **Cool** (cost-efficient, online-archive scenarios).
- **Premium tier** is SSD-backed. For FSLogix profile containers Standard is generally *not* sufficient due to performance constraints; Premium is the practical choice.
- Billing models differ fundamentally: **Premium = provisioned** (pay for all provisioned capacity, 100 GB default minimum, even if idle). **Standard = pay-as-you-go** (pay only for consumed, no minimum).
- Data protection applies to all tiers: multiple copies, zone replication, GEO-redundant (six copies across two regions); incremental share snapshots (up to 200 per share); Microsoft Defender for Storage; encryption in transit and at rest.

*Link to: nerdio-azure-files-premium-autoscale.md, FSLogix design notes.*

*Bron: Nerdio-content 'Azure Files' (Blogs).*

## Verwante notities

- [Azure Files storage redundancy for WVD profiles: LRS vs ZRS vs GRS](azure-files-storage-redundancy-lrs-zrs-grs-2.md)
- [IOPS, latency, and sizing storage for VDI workloads](iops-latency-and-sizing-storage-for-vdi.md)
- [Nerdio Manager storage autoscale for Azure Files Premium](nerdio-azure-files-premium-autoscale.md)
- [Reserved Capacity still leaves you guessing; autoscale is the better answer](position-reserved-capacity-vs-autoscale.md)
