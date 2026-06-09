---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, differencing-disk, identity-disk, write-cache, active-directory]
layer: reference
bron: inside-citrix-fma
---

# MCS Differencing Disk and Identity Disk

Every VM created by MCS consists of two disks attached to it (the exact technical handling differs slightly per hypervisor):

- **Differencing Disk**: stores all changes made to the VM; it functions as a write cache.
- **Identity Disk**: gives the VM its own identity used within Active Directory.

During provisioning, MCS first takes a snapshot of the master VM (automatically, or you can take one manually so you can name it yourself). The snapshot is consolidated (merged) and a temporary VM is created and booted so that tasks like DHCP and KMS can be handled, before being copied over to all datastores in the deployment. MCS also takes care of machine account creation in Active Directory during this phase.
