---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, ups, load-balancing, high-availability, ceip]
layer: reference
bron: inside-citrix-fma
---

# Universal Print Server load balancing and HA (7.9)

Historically the UPS combined with the UPD suited smaller-to-mid-sized companies because before version 7.9 the UPS was a single point of failure with no way to configure multiple print servers for HA/load balancing. XenDesktop/XenApp 7.9 changed this, allowing multiple UPS servers in an LB/HA setup. You must be on a Current Release (not LTSR, which was 7.6 at writing) since base components including VDAs must be updated.

How it works: at login, session (network) printers are mapped to different print servers. Each VDA has a built-in load balancer service distributing print load across all configured print servers per policy. If a print server fails or doesn't respond within a configurable window (default 180 seconds), it's removed from the VDA load-balancing scheme. The load balancer also has a fail-over mechanism that redistributes failed connections to healthy print servers; it's not active/passive HA but part of the load-balancing policy.

Required policies: 'Universal Print Server for load balancing' and 'Universal Print Server out-of-service threshold' (the timeout after which a failed server is considered permanently offline, default 180s). Checks: VDAs periodically PING print servers; a server that can't be reached or fails to respond is considered down. The PING interval is set via a registry key (no policy yet). A manual 'Validate servers' option queries print queue names and verifies servers are identically configured (Citrix recommends identical configuration to optimize printer creation time); validation only logs an event, taking no other action.

Installing UPS automatically enrolls you in the Citrix Experience Improvement Program (CEIP); data is anonymous and encrypted, first upload after 7 days. Opt out via registry HKLM\Software\Citrix\Universal Print Server\CEIPEnabled set to DWORD 0 (1 to opt back in).

FMA fact: multithreading enhancements mean the UPS can now process 80+ print jobs per minute, with reduced resource consumption and improved printer data caching on the VDA.
