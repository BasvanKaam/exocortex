---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [virtualization, snapshot, storage, capacity, fundamentals]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Snapshot Delete Order and Disk Space

The order in which you delete snapshots changes how much temporary disk space the merge consumes.

Delete all snapshots at once: snapshot 3 merges into 2 but is not removed yet, so 2 grows (up to twice its size); 2 then merges into 1 without being removed, so 1 grows substantially; only when 1 finally merges into the original VMDK are all snapshots actually discarded. During this process the chain can temporarily take up to twice as much space.

Delete snapshots one by one: 3 merges into 2 (2 grows) but snapshot 3 is removed immediately, freeing its space before the next merge. This consumes much less temporary space than deleting the whole chain at once.

Practical takeaway from Bas's notes: deleting one at a time is gentler on disk space than collapsing the entire chain in a single operation.

*Bron: Core Knowledge doc 'Virtualisatie Snapshots Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Copy-on-Write Snapshots vs Clones](copy-on-write-snapshots-vs-clones.md)
- [VM Snapshot Mechanics: Delta Files and Redo Logs](vm-snapshot-delta-mechanics.md)
