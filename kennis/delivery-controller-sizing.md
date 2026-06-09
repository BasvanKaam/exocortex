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
