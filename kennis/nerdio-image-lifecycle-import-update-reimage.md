---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, image-management, azure-compute-gallery, fslogix, explainer]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Nerdio image lifecycle: import, update, re-image

How Nerdio Manager handles AVD images end to end. State as of March 2024.

## Image import process
Nerdio orchestrates this as a scripted sequence: set API context, get the source image (Azure Marketplace optional), create a VM plus network, join AD and set time-zone redirection, get configuration and install agents, copy the template VM, create the image VM plus network, clean up the VM, sysprep and capture, create the image object, land it in the Azure Compute Gallery. Script extensions are temporarily added and removed throughout for the install/removal of agents and config/context settings.

## Image update process
The image object is managed and updated through a persistent Image VM (a managed disk). The flow: copy the OS disk to a temp image VM, layer apps via SCCM / App Attach / Intune / scripted actions, sysprep and capture into the Azure Compute Gallery. The ACG can hold multiple image versions and replicas across one or more regions. Two backup mechanisms: back up the Image VM itself via the dropdown menu (multiple backups = restore points), and back up the image object via "Set as image" (copies land under custom images or the unmanaged part of ACG). An ACG image version can be set to "Inactive." The whole update process can be automated and scheduled. Hostpools consume the image object via resize / re-image.

## Re-image process
Per host: set API context, prepare and collect info to remove the VM, log off users, delete the host from AVD, delete the OS disk, get hostpool properties and check the network, create the new VM (includes the image ID) and join to Entra ID, get configuration and install agents, reboot, join to ARM AVD, wait for host creation, activate the AVD host, unjoin from Entra ID, delete the old VM.

Key property worth remembering: users do NOT have to be re-assigned to the hostpool afterwards. The NIC resource isn't touched, so IP addresses and DNS settings do not change across a re-image.

Resources touched across these flows: resource group(s), managed disk(s), storage account(s), key vault(s).

*Bron: Nerdio-content 'Image management' (Innovation Days).*

## Verwante notities

- [AVD Application Management Strategy with Nerdio](avd-application-management-strategy-nerdio.md)
- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-added-value-on-cloud-pc.md)
- [Nerdio Enterprise Optimization Journey (12-step framework)](nerdio-enterprise-optimization-journey.md)
- [Moving images and AVD objects from NME to NMM via Azure tags](nerdio-nme-to-nmm-image-migration-via-tags.md)
- [Patch Tuesday: fully automated image patching in Nerdio](nerdio-patch-tuesday-image-automation.md)
- [Automating the Patch Tuesday image lifecycle in Nerdio](nerdio-patch-tuesday-image-lifecycle-method.md)
- [Nerdio self-service portal: delegated machine control for power users](nerdio-self-service-portal-user-control.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-value-on-top-of-cloud-pc.md)
- [NME persists machine names across reimage/rebuild](nme-hostpool-naming-persistence.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [Start from a fresh image rather than reusing legacy (Citrix) images](start-from-a-fresh-image.md)
