---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [linux-vda, centos, rhel, citrix, xendesktop, testing]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Using CentOS 6.6 to test the Citrix Linux VDA (unsupported but code-close to RHEL)

How it worked then (2015, guest content by Mick Glover, around the Linux VDA dropping in XenApp & XenDesktop 7.6 FP2): the Linux VDA was officially supported only on specific SUSE (SLED/SLES) and Red Hat Enterprise Linux distributions. CentOS 6.6 could nonetheless be used for reproduction and testing because of its close code match to Red Hat, with the bonus of being free and easily accessible. Part 1 covered installing CentOS 6.6 (here as a XenServer 6.5 SP1 VM using the built-in CentOS 6 64-bit template), installing XenServer Tools, setting the hostname in /etc/sysconfig/network, and configuring a static IP via /etc/sysconfig/network-scripts/ifcfg-eth0 (ONBOOT=yes, BOOTPROTO=Static). The durable point: a community/free distro that closely tracks an enterprise one is a legitimate lab substitute for testing even when not officially supported.

*Bron: blogpost '@XDtipster - Linux VDA setup on CentOS 6.6 Pt.1' (2015-07-21), basvankaam.com.*

## Verwante notities

- [Delivering Linux shared hosted desktops: controller, catalog and delivery group setup](linux-vda-controller-and-catalog-config.md)
- [Linux VDA install dependencies and ctxsetup.sh configuration](linux-vda-install-config-dependencies.md)
- [Forcing Microsoft Security Essentials onto Server 2012 (home lab)](mse-on-server-2012-workaround.md)
- [In a PoC the software is easy, the environment is the hard part](poc-setup-the-hard-part-is-the-environment.md)
- [Citrix says supported, Microsoft says not: reading two support matrices at once](vendor-support-matrix-contradictions.md)
