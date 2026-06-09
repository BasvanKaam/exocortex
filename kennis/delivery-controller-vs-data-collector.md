---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [delivery-controller, data-collector, ima, fma, comparison]
layer: reference
bron: inside-citrix-fma
---

# Delivery Controller vs Data Collector differences

A Delivery Controller is fundamentally different from an IMA Data Collector:

- No LHC (prior 2017); uses Connection Leasing. Pulls all static and dynamic info from the Central Site database. (Data Collector caches static and dynamic run-time info locally.)
- Delivery Controllers do NOT communicate with each other and have no scheduled communication with VDAs or the DB, only when needed. (Data Collectors communicate with the IMA store, peer Data Collectors and their Session Hosts within their zone on a schedule or on config change.)
- Responsible only for brokering/maintaining sessions; cannot host user sessions. (Data Collectors often host sessions but can be dedicated.)
- Can run a different OS from the server/desktop VDAs. (Data Collectors must match OS of all Session Hosts and DCs in the Farm.)
- Core services only; the HDX stack is part of the VDA software. (Data Collector has all XenApp 6.5 bits installed.)
- Zones are optional; when configured, each Zone needs at least one Controller. No election applies, deploy at least two per Site/Zone. (Each Zone has one Data Collector; election applies.)
- Has a direct API connection to a hypervisor or cloud platform. (Data Collector has no direct hypervisor/cloud management.)
- Almost all communication flows through the Controller to the Central Site DB. VDAs must successfully register with a Controller. (A booting XenApp server runs the IMA service but does not register anywhere.)

When the Central Site DB is down, no Site-wide config changes are possible; LHC and/or Connection Leasing lets users launch resources successfully started at least once in the prior two weeks.
