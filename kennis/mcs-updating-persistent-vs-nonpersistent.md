---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, persistent, non-persistent, image-update, reboot]
layer: reference
bron: inside-citrix-fma
---

# MCS updating: persistent vs non-persistent VM behaviour

When you update the master image of a persistent VM, only newly provisioned persistent VMs use the updated image. All existing persistent VMs continue to rely on the old master VM.

Non-persistent VMs behave differently: once the new/updated image is assigned and the VMs reboot, the old image is discarded (and eventually deleted once no longer in use) and the new one is used from then on.

Reboots refresh the differencing disk, making it start from zero. Bas advises a reboot schedule for XenApp servers, and rebooting VDI VMs daily or automatically once a user logs off.
