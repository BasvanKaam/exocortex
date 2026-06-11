---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, nutanix, xendesktop, reference-architecture, hsd, hvd, mcs, login-vsi, hyper-v]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Validated Solution: XenDesktop on Nutanix reference architecture

How it was documented in 2014: the 'Citrix XenDesktop on Nutanix' Citrix Validated Solution (CVS) gave prescriptive design, configuration and deployment guidance, validated by the Citrix Consulting APAC team using Login VSI to simulate real-world workloads.

- Covered Citrix's two most popular FlexCast models: Hosted Shared Desktop (multiple users sharing a Windows Server 2008 R2 host) and Hosted Virtual Desktop / VDI (1:1 personal VM), focused mainly on non-persistent desktops.
- Built on XenDesktop 7.1 with Machine Creation Services (MCS) on Hyper-V Server 2012 R2, running on the Nutanix CVM appliance.
- Scale-out scenarios: HSD from 400 up to 1400 users, HVD from 250 up to 1020, depending on node/block count.
- Test hardware: Nutanix NX-3060 nodes, dual-socket 10-core Intel Xeon Ivy Bridge, 128-256GB RAM, dual 10GbE, mixed SSD/HDD, 2U footprint, each node running Windows Server 2012 R2 + Hyper-V + Nutanix Controller VM (CVM).
- Nutanix NOS came in Starter, Pro, and Ultimate editions; the CVS broke the design into User, Access, Desktop, Control, Hypervisor, Network and Hardware layers.

Note of record: Bas emphasises Nutanix is 'a software company before anything else.'

*Bron: blogpost 'Installing and configuring Citrix XenDesktop on the Nutanix computing platform!' (2014-07-08), basvankaam.com.*

## Verwante notities

- [Login VSI and VSImax: benchmarking by saturation](loginvsi-vsimax-saturation-benchmark.md)
- [Nutanix Acropolis is three components, not just a hypervisor](nutanix-acropolis-three-components.md)
- [Nutanix architecture: nodes and Controller VMs](nutanix-controller-vm-architecture.md)
- [Converged (hyperconverged) infrastructure collapses compute and storage into one appliance](nutanix-converged-infrastructure-concept.md)
- [Nutanix is a mature product and here to stay](nutanix-here-to-stay-2014.md)
- [Nutanix's 'new' platform names are partly rebrands of tech they already had](positie-nutanix-rebrands-existing-tech.md)
- [XenDesktop 7 Host Infrastructure and what it unlocks](xendesktop-host-infrastructure-mcs-pvs.md)
