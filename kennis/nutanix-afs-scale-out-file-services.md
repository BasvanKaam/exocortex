---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [nutanix, afs, file-services, fsvm, smb, hci]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Nutanix AFS folds the file server into the HCI cluster

Acropolis File Services (AFS) went GA in Nutanix AOS 5.0 (tech preview in 4.6/4.7) with support for ESXi and AHV. It is a software-defined, scale-out file service running as a core component of the Nutanix platform, so it can run on an existing cluster and eliminates the need for a separate NAS appliance or storage silo. Because it sits on the platform it inherits Nutanix storage features: data tiering, deduplication, erasure coding, compression and distributed self-healing.

Architecture (as of AOS 5.0): a File Server provides the high-level namespace and consists of multiple File Server VMs (FSVMs), minimum three (mirroring the three-node minimum of a Nutanix cluster), each needing at least 4 vCPU and 12GB RAM. Shares sit under the File Server; folders are distributed across the FSVMs. It integrates fully with Active Directory and DNS, supports SMB 2.1 (at the time), Access Based Enumeration, hard/soft quotas with email warnings, Windows Previous Versions self-service, and DR to a secondary cluster. Durable concept (collapse the file server into the storage platform); the specific versions and SMB 2.1-only limit are dated.

*Bron: blogpost 'New in AOS 5.0: Nutanix Acropolis File Services' (2017-01-05), basvankaam.com.*

## Verwante notities

- [Nutanix Acropolis is three components, not just a hypervisor](nutanix-acropolis-three-components.md)
- [Nutanix architecture: nodes and Controller VMs](nutanix-controller-vm-architecture.md)
- [Converged (hyperconverged) infrastructure collapses compute and storage into one appliance](nutanix-converged-infrastructure-concept.md)
- [Nutanix data locality and shadow clones for VDI](nutanix-data-locality-shadow-clones.md)
- [FSVM HA via in-guest iSCSI and DM-MPIO failover](nutanix-fsvm-iscsi-ha-failover.md)
