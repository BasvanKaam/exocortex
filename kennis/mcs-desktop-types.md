---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, desktop-types, pooled, dedicated, catalog]
layer: reference
bron: inside-citrix-fma
---

# MCS desktop types: Pooled-Random, Pooled-Static, Dedicated

Using MCS you can provision three types of desktops (Catalog):

- **Pooled-Random**: a desktop is assigned randomly at logon. On logoff it becomes free for re-use and all changes are lost completely.
- **Pooled-Static**: a desktop is permanently assigned to a user at logon and stays with them after logoff. Any changes made are discarded during reboot/logoff.
- **Dedicated**: a desktop is permanently assigned to a user at logon and stays with them after logoff. Any changes made are saved to the VM no matter how many times it is rebooted or refreshed.

## Verwante notities

- [FlexCast delivery technology, worker types and delivery models](flexcast-delivery-models-and-worker-types.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [MCS Differencing Disk and Identity Disk](mcs-differencing-and-identity-disk.md)
- [MCS updating: persistent vs non-persistent VM behaviour](mcs-updating-persistent-vs-nonpersistent.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [Single-User vs Multi-User VDI/DaaS](single-user-vs-multi-user-vdi-daas.md)
