---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [cwc, cloud-connector, broker, ha, resource-location]
layer: reference
bron: inside-citrix-fma
---

# The CWC Cloud Connector

The Cloud Connector connects VDA resources to the Apps and Desktops Workspace Cloud services. It is made up of several providers/services handling things like registering VDAs and connecting to your on-premises Hypervisor or public cloud platform.

FMA fact: the Cloud Connector is what your VDAs point to and use as a broker, instead of a Delivery Controller in an on-premises deployment.

It installs on a domain-joined Windows Server 2012 R2 machine within one of your Resource Locations (which may itself be cloud-based). Though installed on-premises, it is fully managed by CWC, so it stays patched and current via a light-touch installation. It communicates only over outbound port 443 and can sit behind NAT and web proxy services.

FMA fact: set up at least two Cloud Connectors per Resource Location for HA. No load balancing configuration is needed - CWC sends requests/data to one Connector and, if it gets too busy or stops responding, sends data to the idle Connector or spreads the load across both.

## Verwante notities

- [Citrix Workspace Cloud as the hybrid bridge](citrix-workspace-cloud-hybrid-model.md)
- [Citrix Workspace Cloud (CWC): a managed control plane over the FMA](citrix-workspace-cloud-overview.md)
- [CWC authentication and credential handling security](cwc-authentication-credential-handling.md)
- [Citrix Lifecycle Management Services and blueprints](cwc-lifecycle-management-services.md)
- [CWC StoreFront hosting options](cwc-storefront-options.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
