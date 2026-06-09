---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, image-management, storage, datastores, operations]
layer: rich
bron: inside-citrix-fma
---

# Why MCS image updates matter: every master VM is re-copied to every datastore

Bas stresses the operational cost of MCS image management. Each time you create or update a master VM, the whole snapshot-and-copy process repeats: a snapshot is created and copied over to **all** datastores in the deployment. The system treats an updated master VM as a brand-new master VM.

With multiple master VMs the cost multiplies. His example: two VDI images (Windows 7 and 8) plus two RDSH images (Server 2008 R2 and 2012 R2) means four master VMs, so four snapshots, each copied to every datastore.

He frames the planning questions you must answer to gauge storage and administrative overhead:
- How many master VMs (different OS types) will you manage?
- How many datastores will you use?
- How often (per week/month/year) will master VMs be updated? (always a hard question to answer)
- Does your storage support thin provisioning? If not, every provisioned VM is as big as the master VM it is based on.
