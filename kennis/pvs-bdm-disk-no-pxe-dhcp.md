---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, pvs, bdm, boot, networking]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# BDM disk removes the PXE/DHCP/TFTP dependency for PVS boot

How it worked in PVS 7. In environments where reconfiguring PXE/DHCP is a no-go, the Boot Device Manager (BDM) is the workaround. The concept predates PVS 7, but the configuration was new: no more separate BDM utility. During VM creation via the XenDesktop Setup Wizard you create a BDM partition (a 'BDM disk'), which holds everything needed for the initial boot. No PXE, DHCP or TFTP setup or reconfiguration required. It appears as an xxxbdm.vhdx virtual hard disk attached to the VM.

Related: with Hyper-V 3.0 you still configure a Legacy Network Adapter on the VM, but once the streaming process starts PVS automatically switches the virtual adapter to synthetic mode for better streaming performance.

*Bron: blogpost 'Citrix Provisioning Services 7... A sneak preview' (2013-06-21), basvankaam.com.*

## Verwante notities

- [NetScaler 10.1 TFTP load balancing for PVS boot HA](netscaler-tftp-load-balancing-pvs.md)
