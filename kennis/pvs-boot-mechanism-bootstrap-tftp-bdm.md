---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, bootstrap, tftp, bdm, pxe, dhcp]
layer: reference
bron: inside-citrix-fma
---

# PVS boot mechanism: Bootstrap, TFTP and BDM

A target device finds and contacts a provisioning server using a **Bootstrap file (ARDBP32.BIN)**, which holds everything needed to start streaming, including up to **four** login server IP addresses. The login server (not necessarily the streaming server) then tells the device which server will actually stream the vDisk. The Bootstrap is delivered via **TFTP**.

PVS has its own built-in TFTP server (you can use any). Because the TFTP server is a critical step, make it highly available. Common ways to deliver the TFTP server address:
- **DHCP option 66:** simple, but only one server address — no HA.
- **DHCP option 66 + DNS round robin:** a hostname with multiple A records rotated round-robin (some PXE clients can't handle multiple host entries).
- **PXE (broadcast):** target broadcasts to find a PXE server; if one PVS/PXE server is down the other answers — instant HA without touching DHCP, a very popular approach.
- **Citrix NetScaler:** multiple options to make TFTP highly available.

**BDM (Boot Device Manager):** two methods. (1) PVS generates a small ~300 KB .ISO; target boots from it (e.g. CDROM/DVD) at a shared network location. Uses a two-stage boot where the PVS location is hardcoded into the bootstrap and the rest (PVS drivers) downloads via a proprietary TFTP-based protocol (UDP port 6969). (2) As of XenDesktop 7.0, the XenDesktop setup wizard creates a small **BDM hard disk partition** attached as a separate virtual disk containing all PVS drivers — no two-stage approach, and no PXE/TFTP/DHCP needed (advised for VMs only). BDM also cuts boot times by about **5–10 seconds**.

Full PVS logon/boot sequence: target boots and gets an IP → identifies a TFTP server → downloads and boots from the Bootstrap → logs onto a PVS server → the logon server names the streaming server → target streams the vDisk.

## Verwante notities

- [Provisioning Services essentials and Bas's advice](provisioning-services-essentials.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS high availability](pvs-high-availability.md)
- [PVS provisioning wizards: streamed VM and XenDesktop setup](pvs-provisioning-wizards.md)
- [PVS terminology: Farm, Site, Store, Device Collection, Target Device](pvs-terminology-farm-site-store-collection.md)
- [PVS vDisk creation, Standard vs Private Image Mode](pvs-vdisk-standard-vs-private-image-mode.md)
