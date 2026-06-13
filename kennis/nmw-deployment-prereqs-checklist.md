---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nmw, avd, wvd, deployment, azure, dated]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# NMW Deployment: What to Have Ready Before You Install

Bas's field-prep checklist for getting Nerdio Manager for WVD installed cleanly the first time, distilled from running deployments. The pattern (line up identity, subscription rights, network reachability, and storage before you start the clock) outlives the specific product version.

## Identity and rights
- The installing account must be logged into Azure AD as a Global Administrator with MFA disabled for the install window only. Credentials are not saved; MFA can be turned back on afterwards.
- Conditional Access can block the install too, watch for it.
- The account needs Owner on the target Azure subscription.
- The WVD/AVD app must be registered in the tenant.

## Subscription must be able to deploy
NMW stands up Azure SQL, a Web App, Key Vault, Application Insights, and an Automation account in the selected region. Confirm the subscription can deploy all of these there. If something fails, check that the relevant resource providers are registered, then retry once the deployment finishes.

## Line these up while the deployment runs
- Domain for the session hosts to join (on-prem).
- An FQDN service account for adding/removing machines in AD.
- The OU path to store the machines (set via advanced AD settings).
- The FSLogix profile-container path in FQDN format, in the same region as the WVD hosts.
- A resource group with a proper vNet and subnet that can reach AD; the subnet must point to an AD-aware DNS.

## Image notes
- Start with a new image rather than an existing one in most cases.
- A VM disk must be a managed disk before its SAS URL will work; if you have a VHD, mount it via a VM and create a managed disk from it. To export: add the disk via storage blob (browse to the VHD), then export the disk / generate the SAS URL and copy it.
- The image-build VM never powers on, so size is cheap (a D2s on standard HDD is fine).
- Disable FSLogix in NMW if you already run it elsewhere.

## Gotchas
- If the install hangs on a VM extension, find that extension on the Azure VM and remove it, then let the process finish or retry.
- Fall vs Spring release matters: for Spring, make sure the Microsoft.DesktopVirtualization provider is registered.
- If all else fails, start over from the Azure Marketplace.

*Bron: Nerdio-content 'NMW Deployment steps' ((root)).*

## Verwante notities

- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [Nerdio Manager for WVD deploys into your own Azure tenant](nerdio-manager-wvd-deploys-in-your-tenant.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [NMW architecture: PaaS-only deploy, metering-only billing](nmw-paas-architecture-and-billing-model.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [WVD tenant setup gotchas (2019 workshop)](wvd-tenant-setup-gotchas-2019.md)
