---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, vdisk, versioning, differencing-disk]
layer: reference
bron: inside-citrix-fma
---

# PVS vDisk versioning and lifecycle

A vDisk lifecycle: create and assign, then maintain/update over time, then retire when no longer used. For updating a Standard-mode (read-only) vDisk, PVS **Versioning** creates a new version (a **differencing disk**) linked to the original. You assign the new version to the Master Target Device, boot it in **maintenance mode**, make changes, then shut down. The updated version is **promoted** to Test or Production (can be automated/scheduled). With 'Immediate' promotion target devices must reboot before using the new version; with 'Scheduled' they reboot after the set time/date.

Multiple new versions are all differencing disks pointing back to the original. Citrix advises **merging** the chain back into the base image once you have 3 to a maximum of 5 differencing disks — saving disk space and improving performance. **Merge** options: 'Merged Updates' (merges differencing disks into a new file linked to the original base) or 'Merge Base' (merges base + all differencing disks into one new standalone file). When stored locally, also replicate vDisks to other PVS servers.

Warning: promoting a version actually opens and writes to the vDisk, which can cause inconsistencies if vDisks are stored locally and complicate replication. vDisk updates can be automated/scheduled and support updates from WSUS and SCCM. Once old versions are deleted you cannot revert to them.
