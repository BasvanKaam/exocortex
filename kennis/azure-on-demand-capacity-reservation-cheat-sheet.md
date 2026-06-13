---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [azure, capacity-reservation, reserved-instances, quotas, vm, cheat-sheet, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Azure On-demand Capacity Reservation Cheat Sheet

Bas van Kaam, November 2023. Reusable reference on Azure On-demand Capacity Reservations.

## What they are
- Reserve VM capacity in an Azure region or Availability Zone so the capacity is always available to you. Unlike Reserved Instances, On-demand Capacity Reservations DO come with an SLA.
- No contracts or commitments (unlike Reserved Instances). Start and stop any time; resources are available immediately once capacity is reserved/confirmed.

## Cost
- No discount. You pay the underlying PAYG price for the VMs in the reservation.
- You pay for ALL VMs in the reservation whether they are provisioned or not.

## How they are structured
- Created for a specific VM size/type in a region or Availability Zone. All reservations live inside a Capacity Reservation Group. You pick one VM size/type per reservation but can create as many reservations as you like.
- After configuring, you CAN adjust the number of VMs, but you CANNOT change the VM type or location.
- Can be combined with Reserved Instances and Azure Savings Plans.
- No limit on the number of VMs you can allocate to a reservation.
- Use case: split critical workloads (where a reservation makes sense) from non-critical workloads.

## Not guaranteed at request time
- Requests are not guaranteed. Azure checks availability; if the requested capacity isn't available, the deployment fails.

## Quotas
- Your subscription/region quota must match the number and type of VMs requested (allowed VM count is based on vCPUs).
- View quotas in the Azure portal (search 'Quotas') or via PowerShell/Cloud Shell: `az vm list-usage --location "East US" -o table`.
- VM quotas are defined by vCPUs (cores) consumed. Two main types: regional (vCPUs across VM families in a region) and per-VM-family. There is also an overall VM-count quota per region.
- vCPUs count toward quota for both allocated and de-allocated machines.
- Exceeding any quota makes the reservation request fail.

## Supported / unsupported
- Once accepted, the reservation is available to VMs with matching configurations; the reservation must be specified in the VM's properties.
- Supported VM series (at time of writing): D series (v2 and newer), B, E, F series and a few more; newer preview additions like NV v2+, NC v3+, and Lsv2.
- Supported for a single VM, VM Scale Sets with Uniform Orchestration, and VMSS with Flexible Orchestration (preview).
- NOT supported: Availability Sets, Dedicated Hosts, Spot VMs, Proximity Placement Groups, Update Domains, Ultra-SSD storage, and a few more.
- Free trials, sponsored accounts, and students cannot use Capacity Reservations.

*Bron: Nerdio-content '1701419382305' (Blogs).*

## Verwante notities

- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [Reserved Capacity still leaves you guessing; autoscale is the better answer](position-reserved-capacity-vs-autoscale.md)
- [Shutting Down Reserved Machines Saves Nothing on Compute](position-shutting-down-reserved-machines-saves-nothing.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
- [Reserved Instances Do Not Guarantee Compute Availability](reserved-instances-do-not-guarantee-compute.md)
