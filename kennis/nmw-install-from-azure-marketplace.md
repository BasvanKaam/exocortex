---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmw, install, azure-marketplace, wvd, prereqs]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Installing Nerdio Manager for WVD from the Azure Marketplace

Dated install method for Nerdio Manager for WVD (NMW). Product naming and exact timings reflect the era of writing; verify against current Nerdio docs before reuse.

**Prerequisites (skim before starting):**
- Logged into Azure AD as Global Administrator before deploying via the Marketplace.
- An Azure subscription accessible to that user with Owner role, able to deploy Azure SQL, Web App, Key Vault, Application Insights and an Automation account in the selected region.
- An available virtual network and subnet for the WVD session-host VMs (selected during install).
- Windows Active Directory or Azure AD DS reachable from that vNet; the subnet's custom DNS must point at an AD-aware DNS server.
- Windows AD synchronised with Azure AD.

**Install flow:** Azure Marketplace search for Nerdio, select Nerdio Manager for WVD, run the standard Azure wizard, provide admin credentials.
- **Automated install ("Yes"):** automates most of the install, but requires Conditional Access and MFA to be disabled during installation (re-enable afterwards). A separate throwaway temporary account can be used and discarded once done.
- **Manual ("No"):** generates AzureRM and AZ PowerShell scripts to run locally; you'll be challenged for MFA.
- After Create, deployment takes roughly 20-30 minutes depending on Azure load/region/time of day. Then open Outputs, copy the generated URL, and (for the automated path) run the Automation runbook to finish.

**End-to-end timing Bas quotes:** initial Workspace + hostpool + a few VMs ~15 minutes once NMW is installed; onboarding an existing WVD deployment ~5-15 minutes depending on hostpool/VM count; a full WVD deployment from nothing inside the hour (2-2.5 hours max even without prereqs prepared).

## Related
- nmw-autoscale-engine-capabilities

*Bron: Nerdio-content 'How to deploy a complete WVD environment for your office in minutes instead of days or weeks' (Blogs).*

## Verwante notities

- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [Nerdio Manager for WVD deploys into your own Azure tenant](nerdio-manager-wvd-deploys-in-your-tenant.md)
- [Automating the Patch Tuesday image lifecycle in Nerdio](nerdio-patch-tuesday-image-lifecycle-method.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [What the Nerdio autoscale engine does (NMW era)](nmw-autoscale-engine-capabilities.md)
- [NMW Community Edition: what it is and how to run it on a budget](nmw-community-edition-explainer.md)
- [NMW Deployment: What to Have Ready Before You Install](nmw-deployment-prereqs-checklist.md)
- [NMW architecture: PaaS-only deploy, metering-only billing](nmw-paas-architecture-and-billing-model.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [Why Windows 365 enablement needs Global Admin (org consent)](windows-365-enablement-permissions.md)
