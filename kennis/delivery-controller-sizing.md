---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [delivery-controller, sizing, supported-os, scalability]
layer: reference
bron: inside-citrix-fma
---

# Delivery Controller server sizing and supported OS

Citrix testing shows a relatively light VM can handle up to 5000 desktops per Delivery Controller per hour for user authentication, enumeration and resource launch.

Indicative sizing:
- Processor: 4 vCPUs
- Memory: 4 GB RAM (minimum)
- Network: bonded virtual NIC
- Storage: 40 GB
- OS: Windows Server 2012 R2
- XenDesktop edition: 7.x

Officially supported/tested Delivery Controller operating systems:
- Windows Server 2012 R2, Standard and Datacenter
- Windows Server 2012, Standard and Datacenter
- Windows Server 2008 R2 SP1, Standard, Enterprise and Datacenter

## Verwante notities

- [The XenDesktop Central Site database](central-site-database-role.md)
- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [Delivery Controller as the heart of the FMA](delivery-controller-is-heart-of-fma.md)
- [FMA database sizing numbers](fma-database-sizing-numbers.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [Sizing resources: XenDesktop Design Handbook and community calculators](sizing-resources-and-handbook.md)
- [StoreFront server sizing and supported OSes](storefront-server-sizing.md)
- [VDA install options and supported operating systems](vda-install-options-and-supported-os.md)
