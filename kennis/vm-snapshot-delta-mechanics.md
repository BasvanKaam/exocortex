---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [virtualization, snapshot, hyper-v, vmware, storage, fundamentals]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# VM Snapshot Mechanics: Delta Files and Redo Logs

Both Hyper-V and VMware use snapshots built from delta files (redo logs).

Taking snapshots:
- Snapshot 1 is taken (the parent); as data changes, a redo log fills and snapshot 1 grows.
- Snapshot 2 is taken; snapshot 1 becomes read-only and new changes go into snapshot 2's redo log.
- Snapshot 3 is taken; snapshot 2 becomes read-only, and so on. Each new snapshot freezes the previous chain read-only and captures changes from that point forward.

Reverting:
- Revert from snapshot 3 back to snapshot 1: the changes saved since that point are discarded, the redo log is emptied, and a fresh redo log starts tracking changes again. The original snapshot stays read-only.
- Each revert empties the current delta and starts a new one; older snapshot redo logs stay read-only.
- Only when a new snapshot is taken does the data accumulated up to that point become read-only again.

This is the redo-log behavior an admin has to reason about when managing snapshot trees.

*Bron: Core Knowledge doc 'Virtualisatie Snapshots Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Copy-on-Write Snapshots vs Clones](copy-on-write-snapshots-vs-clones.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [PVS vDisk versioning and lifecycle](pvs-vdisk-versioning-lifecycle.md)
- [Snapshot Delete Order and Disk Space](vm-snapshot-delete-order-space.md)
