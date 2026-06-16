---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [snapshot, copy-on-write, backup, storage, fundamentals]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Copy-on-Write Snapshots vs Clones

The key difference between a clone and a snapshot: a snapshot is not fully independent of the original data, while a clone is.

A snapshot defines a marker at a point in time and ensures data can be rolled back to that point. You can keep multiple snapshots, and they typically need much less extra disk space than clones.

The most common method is copy-on-write: define the snapshot at a point in time, then monitor the original dataset for changes. When a change is made, it is recorded in a separate location. The snapshot therefore grows over time, especially for a quickly changing dataset. A snapshot manager can present different views of the data as if they were full backups, and switch between them on demand.

The crucial caveat: a snapshot is not an independent copy. If the original data is destroyed or corrupted, the snapshot is useless because it only holds recent changes. A snapshot gives you a rollback mechanism, not a real backup. The advantage is speed (you only write changes); the disadvantage is no recoverable backup if the source is corrupted.

*Bron: Core Knowledge doc 'Virtualisatie Snapshots Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [How memory works in Terminal Server: shared executables](terminal-server-memory-shared-executables.md)
- [Why the page file matters in Terminal Server](terminal-server-page-file-copy-on-write.md)
- [Snapshot Delete Order and Disk Space](vm-snapshot-delete-order-space.md)
- [VM Snapshot Mechanics: Delta Files and Redo Logs](vm-snapshot-delta-mechanics.md)
- [Windows Server Backup and VSS Block-Level Imaging](windows-server-backup-vss-block-level.md)
