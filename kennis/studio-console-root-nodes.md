---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-studio, machine-catalogs, delivery-groups, appdisks, delegated-administration]
layer: reference
bron: inside-citrix-fma
---

# Citrix Studio console root nodes

Walking Studio's console root top to bottom:

- Search: machines, Catalogs, applications, sessions, plug-in versions, OSes, Agents, Delivery Groups, users, IP addresses, etc. Searches can be saved.
- Machine Catalogs: collections of virtual/physical machines from which apps/desktops are published; managed as a single entity. One OS per Catalog. Provisioning by hand, MCS or PVS.
- AppDisks: based on application-layering technology, available as of XenDesktop 7.8, created/managed/assigned directly from Studio (no separate console).
- Delivery Groups: assign resources to users. Requires at least one Machine Catalog with an unassigned machine. A machine can belong to only one Delivery Group. Can include AppDisks and App-V apps.
- Applications: manage published apps (add, change, delete, properties, tags, search, move, rename, disable, folders).
- Policies: configure Citrix policies; seven predefined templates; comparison and modelling; RSOP only via GPMC; policies exportable.
- Logging: track admin activities; custom reports in CSV/HTML.
- Configuration: a placeholder node exposing advanced options (and the Customer Experience Improvement Programme toggle).
