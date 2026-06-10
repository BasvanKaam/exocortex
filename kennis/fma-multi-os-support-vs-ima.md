---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, machine-catalogs, operating-systems, ima]
layer: reference
bron: inside-citrix-fma
---

# FMA multi-OS and mixed Machine Catalog support vs IMA

Unlike the IMA, where an entire XenApp Farm had to run the same server OS, the FMA supports multiple operating systems and lets you configure multiple Machine Catalogs each with a different OS within the same Site. Supported OSes mentioned include Windows Server 2012 R2 and Windows 8, 8.1 and 10 (2018 update adds Server 2016 and multiple Windows 10 versions).

Additionally, the Delivery Controller can run a different OS from the Session Hosts/VDAs it communicates with, another difference from the IMA where Data Collectors and Session Hosts in a Farm had to match.

## Verwante notities

- [IMA-to-FMA terminology mapping table](ima-vs-fma-terminology-mapping.md)
