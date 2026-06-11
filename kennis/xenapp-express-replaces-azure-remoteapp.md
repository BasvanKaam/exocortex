---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [citrix, azure, azure-remoteapp, xenapp-express, citrix-cloud, daas]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenApp Express: the Citrix/Microsoft replacement for Azure RemoteApp

How it worked then (announced Aug 2016): Microsoft stopped selling Azure RemoteApp (ARA) after 1 Oct 2016, with existing customers supported until 31 Aug 2017. The replacement, temporarily called Citrix XenApp Express (also "RemoteApp 2.0"), was a joint Citrix/Microsoft cloud service. Key facts as known at the time:
- Exclusive to Microsoft Azure, sold through the Azure marketplace with various instance types.
- Customers bring their own Azure subscription (the resource location), but the control plane is operated exclusively from Citrix Cloud, linked via a Cloud Connector.
- A new simplified management UI (a cut-down Studio) and limited Director monitoring, with a limited number of Catalogs, following the ARA Collection model.
- Distinct from the existing Citrix Cloud XenApp/XenDesktop services. Being XenApp, it published apps only -- no desktop provisioning (that was the separate XenDesktop service plus the announced Windows 10 VDI on Azure).
- An early Tech Preview was due in Q4 2016, with a full showcase at Ignite on 26 Sep 2016.

This is an early waypoint on the road that eventually became Citrix DaaS / Azure Virtual Desktop territory.

*Bron: blogpost 'XenApp Express replaces Microsoft Azure RemoteApp - the facts so far' (2016-08-17), basvankaam.com.*

## Verwante notities

- [New FMA features go to the cloud first](cloud-first-feature-delivery-citrix.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
- [WVD is not a near-term threat to Citrix; enterprise features still favor CTX](wvd-not-a-near-term-threat-to-citrix.md)
