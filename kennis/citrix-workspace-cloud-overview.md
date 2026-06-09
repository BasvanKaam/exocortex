---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [cwc, workspace-cloud, fma, hybrid-cloud, daas]
layer: reference
bron: inside-citrix-fma
---

# Citrix Workspace Cloud (CWC): a managed control plane over the FMA

Citrix Workspace Cloud (CWC) relies heavily on the FlexCast Management Architecture; as soon as Citrix introduces a new FMA feature, CWC gets it first, thanks to a phased 'bucket' approach (still under NDA at the book's writing). It is more a managed/management platform than a product, offering services: Apps and Desktops (XenDesktop/XenApp), Mobility Management (XenMobile), Secure Documents (ShareFile), and Life Cycle Management.

Architecture:
- The CWC control centre / control plane sits at the top of the stack; admins use it to manage and configure deployments.
- Resource Locations hold the VDAs, data and applications, owned and controlled by the customer or partner (e.g. a CSP). They can be on-premises, in a datacentre, or in public/private cloud.
- Resource Locations connect to the CWC services platform via Cloud Connectors.

The model: take a normal XenDesktop/XenApp deployment and 'cloudify' the infrastructural/management pieces. Delivery Controllers, SQL database, License Server, Studio, Director and/or StoreFront live up in CWC as part of the Apps and Desktops service; Citrix sets up, configures, manages and maintains them. The customer is left with only VDAs and NetScaler, hosted anywhere they like. Bas calls it the ultimate hybrid cloud model and 'the way forward'. There was also an AppDisks Tech Preview for CWC.
