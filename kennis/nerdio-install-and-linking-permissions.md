---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nme, azure, permissions, entra, install]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Permissions to Install and Operate Nerdio (NME)

Field reference on what NME actually needs. (Dated: reflects NME v6.0-era behavior, March 2024.)

## Install
- The automated Azure Marketplace install needs **Global Administrator**. There is pushback on this, so Nerdio offers **advanced install methods** that delegate the app creation/registration to another team or person.
- Why Global Admin and not Application Administrator: the App Admin role can grant consent for delegated and application permissions, but **cannot grant consent for Microsoft Graph application permissions** (it can request them, not grant them).

## Linking resources (the permissions Nerdio looks for)
- **Azure Subscription**: Backup Reader & Reader
- **Resource Group**: Contributor
- **Virtual Network**: Contributor or Network Contributor

If Nerdio lacks one of these when linking, it tries to add it automatically using the privileges of the admin doing the linking. For that auto-add, the admin needs **Owner** or **User Access Administrator** on the resource (this is only to grant Nerdio's permission; Owner/UAA is never granted to Nerdio itself). Alternatively, someone with the right privileges can manually add Nerdio's app to the resources; then anyone with at least Reader can link successfully.

## Resources needing Owner
Beyond linking, only two resource types need more: **App Groups** (including the default App Group of a new Host Pool) and **Azure Files**. To manage user role assignments here, Nerdio expects **Owner** on those individual resources. If the admin can't grant role assignments, Nerdio can create the resource but cannot manage user assignments (e.g. cannot add users to the app group). There's a KB on the resulting "Insufficient Permissions to Modify Assignments" error.

Once Nerdio has the right permissions on a resource, the environment can be operated by users with **no Azure permissions at all**.

## Audit attribution: swap to the user
By default the Nerdio app makes all Azure changes, including user-initiated ones. An app setting can **swap** this so user-initiated manual actions show in Azure audit logs as the logged-in user (e.g. a user powering on a VM shows as that user starting the VM). This does not replace the permissions Nerdio needs, and it only applies to manual actions: **automated/background tasks (autoscale, auto-heal, creating/removing VMs) still run under Nerdio's principal**. If swapped, the user must actually have permission for the action or it errors.

## Consent scoping
- Consent is given at **tenant level** during install/final config and **cannot be scoped to subscription level**. Permissions can be revoked afterward in the Azure portal.
- API permissions **cannot be scoped to groups** (Microsoft doesn't support this); they are global. Nerdio's workaround (NME v6.0, Intune only) is to make the application an **owner of the target groups**.
- NME v6.0 added **granular Intune permission assignment** for UEM: customers assign only the permissions they need.

## Revoking permissions
Customers increasingly want to revoke permissions their security team dislikes. Be careful: it is not always clear what will break or what errors NME will show. Testing is mandatory for any API permission change.

*Bron: Nerdio-content 'CORE DOC... Permissions' (Core Docs).*

## Verwante notities

- [Delegated vs Application Permissions (Microsoft Graph)](delegated-vs-application-permissions-graph.md)
- [Setting up MSIX App Attach v2 in Nerdio and publishing apps](msix-appattach-v2-publish-nerdio.md)
- [Azure API limits and Nerdio's API Limit Booster](nerdio-azure-api-limit-booster.md)
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [NME first-admin RBAC and log analytics retention savings](nme-rbac-first-admin-and-savings.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [NMM Partner API: Scope and Enablement Essentials](nmm-partner-api-scope-and-enablement.md)
- [NMW Deployment: What to Have Ready Before You Install](nmw-deployment-prereqs-checklist.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [Always Test Before Revoking API Permissions](positie-test-before-revoking-api-permissions.md)
- [Why Windows 365 enablement needs Global Admin (org consent)](windows-365-enablement-permissions.md)
