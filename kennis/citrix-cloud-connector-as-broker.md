---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-16
tags: [citrix, cloud-connector, workspace-cloud, citrix-cloud, broker, fma, inside-citrix]
layer: reference
gedateerd: ja
bron: inside-citrix-book
---

# Citrix Cloud Connector replaces the on-prem Delivery Controller as broker

How it worked circa 2015-2016 in Citrix Workspace Cloud. The Cloud Connector is the component sitting in a customer Resource Location that connects local VDA resources up to the CWC services. Key point: the VDAs point at the Cloud Connector and use it as their broker, taking the place the Delivery Controller occupies in a fully on-prem deployment.

- Installed on a domain-joined Windows Server 2012 R2 machine inside a Resource Location (which can itself be cloud-based). Light-touch install.
- Fully managed from CWC, so it stays patched and current automatically.
- Outbound communication only, secure, over port 443. Can sit behind NAT and web proxies.
- Bundles several providers/services: VDA registration, and connecting into the on-prem hypervisor or public cloud platform.
- HA: deploy at least two Cloud Connectors per Resource Location. No load balancing to configure; CWC sends work to one and shifts to the idle one if it gets busy or stops responding, or spreads load across both.

*Bron: Inside Citrix (2016), 'Inside Citrix ch25 - Citrix Workspace Cloud'.*

## Verwante notities

- [Citrix Lifecycle Management blueprints](citrix-lifecycle-management-blueprints.md)
- [Citrix Workspace Cloud control plane and resource locations](citrix-workspace-cloud-control-plane-resource-locations.md)
- [Citrix Workspace Cloud credential and authentication handling](citrix-workspace-cloud-credential-handling.md)
- [Citrix Workspace Cloud (CWC): a managed control plane over the FMA](citrix-workspace-cloud-overview.md)
- [The CWC Cloud Connector](cwc-cloud-connector.md)
- [Delivery Controller as the heart of the FMA](delivery-controller-is-heart-of-fma.md)
- [VDA registration and Controller discovery order](vda-registration-and-controller-discovery.md)
