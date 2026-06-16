---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nme, avd, troubleshooting, permissions, tenant, cheat-sheet]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# NME / AVD troubleshooting cheat sheet

Field fixes I keep handy for NME/AVD installs and operations.

## Install / tenant / subscription errors
- Confirm `Connect-AzAccount` has actually logged in; verify tenant and subscription: `Get-AzTenant` (tenant details), `Get-AzSubscription` (subs you can access), `Set-AzContext [-Tenant <id>] [-Subscription <id>]`.
- Could be a permission issue: check it's not a guest account, and check Conditional Access.
- CSP accounts with multiple identity tenants mapped can fail install. Workaround: create a fresh account with Owner permission; NME then installs cleanly.
- "Two apps with the same Windows Azure Service Management API name" in the tenant also causes install errors; resolve the duplicate.
- **Cloud Shell vs local PowerShell**: Cloud Shell defaults to the tenant you signed into. `Get-AzContext` shows connected tenants. `Disconnect-AzAccount` can disconnect the wrong one. With guest accounts across several tenants, `Get-AzSubscription` may not list all subs (rare: guest lacks read access).

## Permissions
- **Assigning a desktop to a user fails**: the NME app needs **Owner on the resource group that contains the host pool** – setting permissions on the RG that holds the VMs is not enough.
- **App Attach assignment issues**: usually the NME App Service lacks Owner on the resource group. NME tries to add this via the logged-in admin; if that admin lacks the rights, it won't happen and you must assign it separately.
- **Subscribing NME**: unless full consent was given during install, subscription Owner is usually enough to subscribe; otherwise a Global Admin account may be needed.

## Backups / images
- **"Manage backups" missing on Desktop Images**: doesn't show for powered-on VMs and throws a warning on power-on. Workaround: manually create an RSV, apply the tags, enable backup against one Desktop Image manually; once done the functions start appearing.
- **Using existing (e.g. Citrix) images**: often fails. Best practice is to start from a fresh image. May work via import + creating an image object through Nerdio, or building a new host pool on that image; installing apps on it can break it, removing apps and retrying may recover it.
- **Change VM SKU of an existing personal-persistent machine**: snapshot the disk, deploy a new VM from the snapshot. For multi-session, a redeploy is the better option.

## Networking / identity
- **Network selection not offered**: if only one network is linked in Nerdio, there's nothing to choose – expected.
- **Entra-ID not supported across multiple domains added to NME**: with Entra-ID auth, network and resource group are greyed out; switching identity back to hybrid restores the network → RG selection. A second non-Entra tenant (ADDS/AD) needs line of sight to identity (VPN or connectivity to the identity tenant).
- **Can't find/select groups for resource assignment**: for Entra-ID this must be enabled in NME; could also be an Entra entitlement, or the resources being co-managed by another tool (e.g. Intune). Identity must live in the **main tenant where NME is installed** – don't install NME into a second resource tenant and then try to add the identity tenant.

## Misc
- **NME extension blob storage** stores the Nerdio AVD agent, FSLogix, Sepago, scripts and sysprep for image creation.
- **Pre-stage host OS disks** timing is based on the time zone of the autoscale configuration setting.

*Bron: Nerdio-content 'Troubleshooting' (Troubeshooting).*

## Verwante notities

- [Delegated vs Application Permissions (Microsoft Graph)](delegated-vs-application-permissions-graph.md)
- [Setting up MSIX App Attach v2 in Nerdio and publishing apps](msix-appattach-v2-publish-nerdio.md)
- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [NME first-admin RBAC and log analytics retention savings](nme-rbac-first-admin-and-savings.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [Always Test Before Revoking API Permissions](positie-test-before-revoking-api-permissions.md)
- [Start from a fresh image rather than reusing legacy (Citrix) images](start-from-a-fresh-image.md)
