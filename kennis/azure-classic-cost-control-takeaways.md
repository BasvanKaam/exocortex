---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure, cost, vm, billing, test-lab]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Azure cost-control habits for a test lab

How it worked then (2015): the free trial gave ~150 euros over 32 days, which Bas found went a long way. Key cost behaviors he documented: VMs are billed only while running; to stop billing for compute you must shut a VM down from the Azure portal to reach the "Stopped (de-allocated)" state. Shutting down from inside the guest OS is NOT enough. Even de-allocated, the VHD storage holding the OS is still charged (but little). Internal and inbound network traffic is free; only outbound is charged, with the first 5 GB outbound free. A small A0 domain controller could run 24x7 for roughly 10 euros a month; a standard D1 (1 core, 3.5 GB RAM, 50 GB SSD) cost around 14 euro-cents per hour. PowerShell scripts could schedule machines offline during off-peak hours. The durable principle: in a pay-per-hour cloud, lifecycle discipline (de-allocate when idle) is the main cost lever, and you rarely need fast machines for a lab.

*Bron: blogpost 'How to: Get up to speed with Windows Azure. Deploying your personal test lab, fast!' (2015-06-22), basvankaam.com.*

## Verwante notities

- [Immutable names and per-VM RDP endpoints in classic Azure](azure-classic-immutable-names-and-rdp-endpoints.md)
- [Correct build order for an early Azure test lab](azure-classic-test-lab-build-order.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [Moving to the cloud does not automatically save money](cloud-does-not-automatically-save-money.md)
- [NMW Community Edition: what it is and how to run it on a budget](nmw-community-edition-explainer.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
