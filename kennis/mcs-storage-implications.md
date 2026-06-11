---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, storage, iops, hyper-converged, caching]
layer: rich
bron: inside-citrix-fma
---

# Bas's MCS storage implications checklist

Bas works through a long list of storage considerations for MCS, hard-won from practice. Highlights:

- Caching reads is a very welcome feature. Consider IntelliCache (XenServer) for non-persistent VMs on NFS storage, and Clustered Shared Volumes Cache (Hyper-V), which would probably outperform PVS altogether, with the exception of PVS cache-in-RAM.
- Collect as much IOPS/workload data as possible and consult storage admins. Remember there is more to IOPS than read/write ratios: also consider random vs sequential, block sizes, and actual throughput.
- Multiple datastores are often created to spread IOPS load, but remember each master VM create/update copies to all of them.
- Load testing helps, but don't forget resource-intensive applications excluded from standard baseline tests: "You don't want to run into any surprises when going live, do you? Include them."
- Scale for peaks (boot, logon, logoff storms); pre-boot VDI and virtual XenApp servers before users start.
- Avoid overcommitting host compute. Overcommitting physical CPUs/cores is fine, but never overcommit memory.
- Storage vMotion / Live Storage Migration / Storage XenMotion of MCS VM disks is **not supported**. Renaming network connections and datastores is also not possible.
- There is a strong dependency between the VM and its Disk ID/datastore (stored in the Central Site database); once broken, the VM won't boot properly. Hyper-converged/SDS solutions (Nutanix, Atlantis, VSAN, VPLEX) can move MCS VMs while maintaining the Disk ID dependency via Shadow Clones, Data Locality, etc. "SDS is key."
- Thin provisioning, compression and de-duplication of differencing disks are preferred and storage-platform dependent. With thin provisioning and a small environment (<1000), re-provisioning once or twice a month is optional; you might get a few hundred machines per hour.
- When an image is updated there are temporarily two full master images per datastore: include this in your GB calculations. The old image is deleted automatically once all VMs use the new one, by default after 6 hours (configurable via PowerShell).

## Verwante notities

- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [MCS supported hypervisor storage and thin provisioning limits](mcs-hypervisor-storage-support.md)
- [Why MCS image updates matter: every master VM is re-copied to every datastore](mcs-image-update-repeats-full-copy.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [MCS rollbacks and reboot considerations (boot storms, disconnect policies)](mcs-rollbacks-and-reboot-considerations.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
