---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [ima, fma, terminology, migration, reference-table]
layer: reference
bron: inside-citrix-fma
---

# IMA-to-FMA terminology mapping table

Key component/concept name changes from the IMA to the FMA (note: counterparts do not always deliver identical features):

- Farm to Site
- Data Collector to Delivery Controller
- Zones to Zones (FMA only as of version 7.7)
- Local Host Cache to Connection Leasing
- Session Host / XenApp server to Virtual Delivery Agent (VDA)
- Delivery Services Console / App Center to Citrix Studio and Director
- EdgeSight monitoring to (partly) Director
- Application folders to Application folders and Tags
- Worker Groups to Machine Catalogs / Delivery Groups
- IMA Datastore to Central Site database (SQL only)
- Load evaluators to Load-managed policies
- IMA protocol and services to Virtual Delivery Agents
- Farm Administrators to Delegated Site Administrators
- Citrix Receiver to Citrix Receiver X1
- Smart Auditor to Session recording
- Shadowing to Microsoft Remote Assistance (via Director)
- USB 2.0 to USB 3.0 support

A XenApp Farm (6.5) or XenDesktop/XenApp Site (7.x) is also referred to by Citrix as a 'Deployment'.
