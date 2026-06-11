---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [san, zoning, storage, fibre-channel]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# SAN Zoning: Hard vs Soft Zones

Zoning controls which initiators and targets on a SAN can see each other. You assign aliases to switch ports and to nodes; the state where all switches share the same configuration is the **point of convergence**.

- **Hard zones**: defined by physical **switch port**. Example: a zone built from the first port of each of three switches, using each port's alias as a member. The device is bound to the physical port.
- **Soft zones**: defined by **node aliases** (e.g. HBA and array-controller names). Once the zone is pushed to all switches, the members can connect to any port on any switch and are automatically placed in their soft zone.

Hard zones bind to location; soft zones follow the device.

*Bron: Core Knowledge doc 'NAS - SAN Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Bas's war story: SAN/NAS data migrations were weeks of nightmares](bas-san-nas-nightmares.md)
- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [LUN Masking](lun-masking.md)
- [NAS vs SAN Storage Architectures](nas-vs-san-storage.md)
- [Why traditional SANs are complex for virtual workloads](traditional-san-complexity.md)
