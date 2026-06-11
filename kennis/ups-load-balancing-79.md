---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, printing, universal-print-server, load-balancing, high-availability]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Universal Print Server load balancing and HA (7.9)

How Citrix printing HA changed in XenDesktop/XenApp 7.9 (mid-2016). Before 7.9 the Universal Print Server (UPS) was a single point of failure, no way to run multiple print servers with HA/LB, which is why UPS+UPD was historically positioned for smaller-to-mid companies where printing mattered but wasn't business critical.

7.9 added multiple UPS in an LB/HA setup. Requires a Current Release (not LTSR), since base components including VDAs must be updated.

How it works: at logon, session network printers are mapped to different print servers. Each VDA has its own built-in load balancer service that distributes print load across all configured print servers per policy. Checks run periodically; if a print server fails to respond to PING or can't be reached, and stays unresponsive past the configurable 'out-of-service threshold' (default 180 seconds), it's removed from that VDA's load-balancing scheme. The LB service has built-in failover that redistributes failed print connections to healthy servers, so it's HA via load balancing, not active/passive.

Required policies: 'Universal Print Server for load balancing' and 'Universal Print Server out-of-service threshold'. A 'Validate servers' button queries print servers for queue names and checks they're configured identically (Citrix recommends identical config to optimise printer creation time); validation only logs, takes no other action. The PING interval is set via a registry key, not yet a policy. In theory there's no limit to the number of print servers.

UPS has two parts: UpsClient (built into the VDA, disabled by default, enabled via the 'Universal Print Server enable' policy) and the UpsServer component (installed separately on the print server). The XPS UPD also gained advanced features in 7.9: stapling and paper-tray (draw) selection, when device and native driver support them.

Installing UPS auto-enrols you in the CEIP; opt out via registry HKLM\Software\Citrix\Universal Print Server\CEIPEnabled set to 0 (1 to opt back in).

*Bron: blogpost 'What's new... Printing in Citrix XenDesktop and XenApp 7.9? A more in-depth look.' (2016-06-03), basvankaam.com.*

## Verwante notities

- [Citrix's problem is integration and focus, not lack of products](positie-citrix-should-integrate-not-just-build.md)
- [Printing is business critical, and underrated](printing-is-business-critical.md)
