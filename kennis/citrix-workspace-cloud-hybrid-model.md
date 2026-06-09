---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [cwc, cloud, hybrid, cloud-connector, daas]
layer: rich
bron: inside-citrix-fma
---

# Citrix Workspace Cloud as the hybrid bridge

Bas presents Citrix Workspace Cloud (CWC) as the ultimate hybrid model and an easy on-ramp to the cloud. All the latest FMA features (and ShareFile, XenMobile) land in CWC first before reaching the on-premises XenApp/XenDesktop products, via a simple updating/testing mechanism still under NDA at time of writing. CWC consoles look and feel identical to on-premises Studio and Director.

Architecture: instead of pointing VDAs at a Delivery Controller, they point at a Cloud Connector as their broker. You need at least two Cloud Connectors per Resource Location for HA, with no load balancing to configure — CWC sends data to one and shifts to the other (or spreads load) if it gets busy or unresponsive. Each tenant's metadata is stored separately and secured with unique credentials. Resource Locations include on-premises datacentres, Azure, AWS and the Citrix CloudPlatform. CWC supports both MCS and PVS for provisioning, and ships out-of-the-box blueprints for XenDesktop, XenApp, XenMobile, NetScaler and the Workspace Suite.

Bas argues CWC gets you close to desktop-OS-based DaaS: host the infrastructure in the cloud while using your own on-premises VDAs, which can be 100% desktop-OS VDI — sidestepping Microsoft's licensing limits on true cloud VDI.
