---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-director, scom, comtrade, insight-services, call-home]
layer: reference
bron: inside-citrix-fma
---

# Director SCOM and Insight Services integration

SCOM integration: as of version 7.7, SCOM alerts integrate directly into Director (only SCOM 2012 R2 supported at time of writing). SCOM alerts appear alongside Citrix alerts, showing severity, time raised, name and source, with a dedicated SCOM tab for filtering by management pack, machine source, severity and time period. The SCOM web interface can be launched from Director's Alerts page. All alerts export to PDF, CSV or Excel.

Comtrade SCOM management packs: Citrix acquired the Comtrade SCOM management packs. Available exclusively from Citrix (Platinum XenDesktop/XenApp only): XenApp, XenDesktop, NetScaler, XenMobile, ShareFile, XenServer, StoreFront, Web Interface, Provisioning Services, License Server and CloudBridge. They integrate Director's helpdesk capabilities and add infrastructure/workload monitoring, end-to-end Citrix infrastructure monitoring, SLA dashboards across sites/versions, advanced app/delivery-group/site and user-experience monitoring, and Director launch from the management pack GUI.

Insight Services: as of version 7.8, Citrix Insight Services (cis.citrix.com) is accessible from a Director drop-down, collecting data from Citrix Scout and Call Home services. Call Home periodically collects systems/product configuration plus performance, error and other info, sent to Insight Services for proactive analysis. The FMA analytics service plays a key role here.

FMA fact: Director can also monitor IMA-based XenApp 6.5 architectures (shadow sessions, machine details pane, HDX panel, delegated administration, Activity Manager for 6.5).
