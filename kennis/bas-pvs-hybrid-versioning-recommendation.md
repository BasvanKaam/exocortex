---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, vdisk, versioning, best-practice, positie]
layer: rich
bron: inside-citrix-fma
---

# Bas's PVS recommendation: hybrid versioning approach

Bas shares a hands-on, hard-won recommendation for managing PVS vDisks. It's not uncommon to see 'old school' system administrators using the fully manual approach — copying and editing multiple vDisks — instead of PVS Versioning.

In larger environments he often sees, and recommends, a **hybrid deployment**: use **Versioning** for test and development environments, but for **production** apply the **manual full-vDisk-copy** approach. This sidesteps the risk that promoting a version opens and writes to the live vDisk (which can cause inconsistencies and complicate replication when vDisks are stored locally).

His underlying advice in either case: first get yourself thoroughly familiar with the process and the steps involved, one at a time.

## Verwante notities

- [MCS updating: persistent vs non-persistent VM behaviour](mcs-updating-persistent-vs-nonpersistent.md)
- [Provisioning Services essentials and Bas's advice](provisioning-services-essentials.md)
- [Bas's PVS key takeaways and best-practice asides](provisioning-services-key-takeaways.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS high availability](pvs-high-availability.md)
- [PVS vDisk creation, Standard vs Private Image Mode](pvs-vdisk-standard-vs-private-image-mode.md)
- [PVS vDisk versioning and lifecycle](pvs-vdisk-versioning-lifecycle.md)
