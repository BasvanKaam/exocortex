---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [storage, nas, san, architecture]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# NAS vs SAN Storage Architectures

- **NAS (Network-Attached Storage)**: a full file server on the network, using TCP/IP. The file system is managed by the NAS device itself and exposed over file-oriented protocols like NFS or SMB/CIFS - clients request part of a file. Any networked machine can connect, which makes cross-OS sharing easy, and capacity scales by adding/linking units. Purpose-built NAS OSes outperform a general file server and use less power.
- **SAN (Storage Area Network)**: an architecture coupling servers (initiators) to storage devices (targets: disk arrays, tape libraries, optical jukeboxes) at the **block** level, so the OS sees the storage as if directly attached. Because compute and storage are physically decoupled, storage can be managed without taking servers offline, and the SAN can be made redundant.
- **DAS (Direct-Attached Storage)** is the third option: storage wired directly to one machine.

Key distinction: NAS serves files, SAN serves blocks.

*Bron: Core Knowledge doc 'NAS - SAN Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DFS Namespace: Roots, Links, and Targets](dfs-namespace-roots-links-targets.md)
- [LUN Masking](lun-masking.md)
- [RAID Levels Overview](raid-levels-overview.md)
- [SAN Zoning: Hard vs Soft Zones](san-zoning-hard-soft.md)
