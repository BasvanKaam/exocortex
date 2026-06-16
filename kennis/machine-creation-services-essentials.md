---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, differencing-disk, storage, application-layering]
layer: reference
bron: inside-citrix-fma
---

# Machine Creation Services essentials

MCS is considered easy: managed and configured directly from Studio with no additional infrastructure (unlike PVS). It is based on differencing-disk technology and works only with virtual machines. The base/golden image is copied to every datastore in the deployment, so plan storage accordingly. Rollbacks are treated like a new/updated base image and copied to all datastores — unless the previous image is still in use by some machines, in which case no full copy is needed.

When application virtualisation is not an option (forcing apps into the base image), consider application layering as an alternative. Give Idle and Disconnect session policies thought to make night-time reboots easier. MCS can be used with Azure, AWS and the Citrix CloudPlatform (PVS cannot — it simply does not work in those clouds), and with all listed hypervisors.

## Verwante notities

- [The key line between Essentials and full Citrix Cloud: VDA placement](essentials-vs-full-citrix-cloud-vda-placement.md)
- [Host Connections now support cloud, not just hypervisors](host-connections-cloud-support.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [Bas on MCS, workloads and the case for application layering](mcs-application-workloads-layering.md)
- [MCS Differencing Disk and Identity Disk](mcs-differencing-and-identity-disk.md)
- [Why MCS image updates matter: every master VM is re-copied to every datastore](mcs-image-update-repeats-full-copy.md)
- [MCS updating: persistent vs non-persistent VM behaviour](mcs-updating-persistent-vs-nonpersistent.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
