---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [azure-migrate, data-box, azcopy, blob-storage, expressroute, migration]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Azure data migration and import tools

Moving data into the cloud varies per situation. Note: Microsoft 365 was renamed in 2020 (formerly Office 365); because most companies already use such cloud services, much data already sits in Azure, easing the rest of the move. Remaining data is often application, database, archive and user-profile data (e.g. FSLogix).

Azure import/migration tooling Bas lists:
- Azure Migrate: a suite to plan, migrate and manage migrations of on-prem infrastructure (VMs, databases) to Azure; supports VMware, Hyper-V and physical systems to Azure VMs and managed databases.
- Azure Site Recovery (ASR): built for disaster recovery but often used for migrations via continuous VM replication; lets you pick the cut-over moment precisely.
- Azure Data Box: physical appliances (Data Box, Data Box Disk, Data Box Heavy) for large volumes (terabytes to petabytes) - copy data to the device and ship it to Microsoft for secure upload.
- Azure Storage Explorer: desktop app with a GUI to upload and manage data, blobs, and move files between cloud storage locations.
- Azure Import/Export Service: ship your own hard drive to Microsoft to import data into Azure; an alternative to Data Box for smaller amounts.
- Azure Blob Storage + File Sync: Blob for unstructured data (images, video, logs), uploadable via REST API, Azure PowerShell or AzCopy; File Sync syncs on-prem files to Azure File Storage.
- AzCopy: command-line tool for copying files to/between Azure storage accounts; efficient for bulk transfers to blob, file and table storage.
- Azure Database Migration Service: online and offline migration of SQL Server, MySQL, PostgreSQL etc. to Azure SQL Database, SQL Managed Instance or other targets.
- APIs and SDKs: for developers migrating specific apps programmatically or automating data migration.
- ExpressRoute: a private connection to Azure for large volumes or critical workloads, faster and lower-latency than ordinary internet.

Each provider has its own toolset. As the AWS counterpart to Azure Data Box, Bas mentions the Snowball Mobile (he writes), a sea container full of storage units transported by truck - which he admits he has personally never seen in real life.
