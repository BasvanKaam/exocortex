---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-director, monitoring, troubleshooting, edgesight, hdx-insight]
layer: reference
bron: inside-citrix-fma
---

# Citrix Director: monitoring and troubleshooting tool

Director is a real-time, web-based tool (installable as a website on Delivery Controllers) that lets administrators monitor, troubleshoot (real-time and historical) and perform support tasks for end-users. It is Citrix's 'first line of defense', included by default with all XenDesktop/XenApp editions (higher editions add functionality). As of XenDesktop 7.x it has some former EdgeSight functionality built in (mainly historical reporting), and with Platinum licenses for both XenDesktop and NetScaler you can monitor NetScalers (HDX Insight) from the same console.

By default Director has access to: real-time data from the Broker Agent (unified console with EdgeSight features, Performance Manager, Network Inspector); historical data in the Monitor database plus the Configuration Logging database; ICA data from the NetScaler Gateway via HDX Insight; and Personal vDisk runtime monitoring (including the ability to reset the Personal vDisk as a last resort, using CtxPvdDiag.exe to gather logs). Best practices: CTX139382.
