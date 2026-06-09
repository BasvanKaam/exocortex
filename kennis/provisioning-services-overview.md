---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, single-image-management, vdisk, streaming]
layer: reference
bron: inside-citrix-fma
---

# Citrix Provisioning Services (PVS) overview

For delivering the base OS in Citrix environments you can install/manage manually, automate/script installs, or use **single image management** via Machine Creation Services (MCS) or **Provisioning Services (PVS)**.

PVS is based on **software streaming**: a single read-only **vDisk** (virtual disk) is streamed over the network to many **target devices** (XenApp servers or XenDesktop VDI VMs). You always run at least two provisioning servers for HA, more depending on scale. Just two provisioning servers can provision several hundred or even thousands of physical/virtual machines (though more is preferred).

MCS will be discussed in the next chapter; the PVS chapter is meant as a high-level overview rather than a full setup/management guide.
