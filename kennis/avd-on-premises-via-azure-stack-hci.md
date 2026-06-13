---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, azure-stack-hci, hybrid-cloud, on-premises, nerdio]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Running AVD On-Premises via Azure Stack HCI

The number-one request since AVD (then WVD) went GA on Sept 19, 2019 has been: can we run AVD on-premises? Historically no. Azure Stack HCI changed that.

**Azure Stack HCI** is Microsoft's hyper-converged infrastructure solution that lets organizations run virtualized workloads on-premises while integrating with Azure cloud services, AVD being one of them. It combines storage, compute and networking into a single certified hardware appliance, with most major hardware vendors in the program. Management has the same look and feel as Azure, so think of it as an extension of Azure rather than a separate world.

**Why on-prem AVD at all** (despite cloud's advantages): keeping apps and desktops close to users to minimize latency, and the desire (or feeling) of being in control of the back-end infrastructure.

**Nerdio + Azure Stack HCI** creates a hybrid cloud: cloud-style scalability and flexibility with data and apps kept on-premises. Nerdio still automates deployment and management of AVD and related services (FSLogix, Azure Files shares, monitoring, identity, applications), while HCI simplifies the on-prem infrastructure. The pitch is a consistent user experience across on-prem and cloud, the ability to scale VDI without expensive hardware upgrades, and cost savings from Nerdio's autoscale/automation layered on top.

*Bron: Nerdio-content 'Nerdio and Azure Stack HCI integration part one' (Blogs).*

## Verwante notities

- [Azure Stack HCI (renamed Azure Local): cloud in your own datacenter](azure-stack-hci-azure-local.md)
- [Cloud-First, But On-Prem AVD Has Legitimate Drivers](cloud-first-but-on-prem-has-real-reasons.md)
- [Hybrid/private on-prem (Azure Stack-style) is the model for the next 5-10 years](hybrid-cloud-azure-stack-model-for-next-decade.md)
- [Converged (hyperconverged) infrastructure collapses compute and storage into one appliance](nutanix-converged-infrastructure-concept.md)
- [Cloud-only is a utopia; cloud-first or hybrid is the only honest answer](positie-cloud-only-is-a-utopia.md)
- [Not WVD on-prem, but a pragmatic middle ground](wvd-on-prem-workarounds-positie.md)
