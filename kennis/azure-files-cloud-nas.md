---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [azure-files, azure-file-sync, nas, san, smb, nfs]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Azure Files: a cloud NAS, plus Azure File Sync for hybrid

Azure Files (part of Azure Storage Accounts) is functionally like a NAS but works fully in the cloud. It offers file-share storage in Azure, sharing files over networks via the familiar SMB or NFS protocols, so users and apps access, edit and share files from the cloud rather than a physical on-site device.

Vs NAS/SAN:
- Network file access: like a NAS, with the same familiar protocols and experience as local storage.
- Flexibility/scalability: scalable on demand with (more or less) unlimited capacity, growing dynamically without physical-hardware limits.
- Back-up and management: Azure manages the infrastructure (including back-up data), avoiding the need to maintain your own storage infra and the initial Capex investment.

Azure File Sync couples on-prem fileservers to Azure Files: files are kept locally for fast access while automatically syncing to Azure Files for back-up, scalability and disaster recovery - creating a hybrid environment.

Azure Files can replace a NAS or SAN in many scenarios, especially when you no longer want to buy/manage physical storage or need scalable cloud storage. But for specific cases - very low latency or hardware integrations - companies may still need (or prefer) SAN solutions. Bas notes SAN technology has also not stood still and is no longer comparable to the picture he sketched from 20+ years ago.

## Verwante notities

- [Storage tiering and lifecycle policies cut AWS storage cost](aws-storage-tiering-and-lifecycle-cost.md)
- [The Azure cloud hierarchy: tenant down to resources](azure-cloud-hierarchy.md)
- [Azure data migration and import tools](azure-data-migration-import-tools.md)
- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [Bas's war story: SAN/NAS data migrations were weeks of nightmares](bas-san-nas-nightmares.md)
- [Bas on the future limits of self-hosting your own data growth](bas-self-hosting-data-growth-limit.md)
- [Core cloud building blocks: datacenter, virtualization, APIs, storage, databases, elasticity](core-cloud-components-and-concepts.md)
- [DaaS / VDI Additions to the Technical Design](daas-vdi-technical-design-considerations.md)
