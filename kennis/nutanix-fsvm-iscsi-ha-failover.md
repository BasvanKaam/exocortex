---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [nutanix, fsvm, iscsi, dm-mpio, cvm, high-availability]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FSVM HA via in-guest iSCSI and DM-MPIO failover

How Nutanix AFS high availability worked then: each FSVM uses the Acropolis Volumes API for storage, accessed via in-guest iSCSI, which lets any FSVM connect to any iSCSI target if an FSVM fails. Path availability uses DM-MPIO inside the FSVM, with the active path set to the local CVM by default. If the local CVM becomes unavailable, DM-MPIO activates a failover path to a remote CVM which takes over IO; when the local CVM is healthy again it is re-marked as the active path so IO stays local. A clean example of HCI HA design where data-locality and storage failover are handled below the file-serving layer.

*Bron: blogpost 'New in AOS 5.0: Nutanix Acropolis File Services' (2017-01-05), basvankaam.com.*

## Verwante notities

- [Nutanix AFS folds the file server into the HCI cluster](nutanix-afs-scale-out-file-services.md)
