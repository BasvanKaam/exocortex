---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [san, lun, storage, security]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# LUN Masking

LUN masking hides (masks) LUNs so each server only sees the LUNs you intend it to see, even when zoning would otherwise expose more. It can be enforced at one of three levels:

- The storage array.
- Intelligent bridges or routers.
- HBA drivers.

Zoning controls which devices can talk on the fabric; LUN masking then narrows which specific volumes a host is allowed to see.

*Bron: Core Knowledge doc 'NAS - SAN Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [NAS vs SAN Storage Architectures](nas-vs-san-storage.md)
- [SAN Zoning: Hard vs Soft Zones](san-zoning-hard-soft.md)
- [Why traditional SANs are complex for virtual workloads](traditional-san-complexity.md)
