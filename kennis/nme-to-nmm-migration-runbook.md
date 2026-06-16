---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nme, nmm, msp, avd, migration, fslogix, msix-app-attach]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# NME to NMM migration runbook (AVD)

Bas's ordered checklist for migrating an AVD environment from Nerdio Manager for Enterprise (NME) to Nerdio Manager for MSP (NMM), assuming the tenant stays the same. Product-specific, treat as dated and re-verify against current Nerdio docs before use.

## Steps
1. Install NMM (can run alongside NME in the same tenant).
2. Configure role-based access at the MSP level.
3. Link to the customer tenant where NME is installed. Note: multiple subscriptions are not supported.
4. Link the same networks and resource groups in NMM as used in NME.
5. Select the existing identity solution used in NME (or configure/choose a new one).
6. Unlink Azure Files file shares in NME and link them in NMM; reconfirm autoscaling on Azure Files.
7. Add the FSLogix configuration to NMM using the same resources as NME.
8. Unlink the GitHub repo from NME and link it to NMM at MSP level; replicate needed scripts to the customer tenant; reconfigure secure variables and enable runbooks.
9. Unassign the Workspace, link networks/resource groups in NMM, refresh the page, and associate the AVD environment with NMM.
10. Upload existing NME images into NMM.
11. If needed, configure image management and any scripted actions from NME (set as image, schedule reboots, updates, etc.).
12. Reconfigure autoscale on host pools to point to the newly uploaded images.
13. Point the newly associated host pools to the FSLogix configuration.
14. Configure per-host-pool settings: RDS session settings, FSLogix, monitoring, session time limits, etc. Note: DR is not available from within NMM.
15. Reconfigure FSLogix shrink via runbook if applicable.
16. Import any MSIX App Attach images from NME into NMM, including certificates; assign App Attach apps to AVD hosts. Note: does not work in combination with Azure AD DS.
17. Re-assign users to AVD hosts.
18. Enable and configure monitoring in NMM (per host pool as desired).
19. Fine-tune networking via the networking module.
20. Fine-tune backup via the backup module/settings.
21. Configure Intune if desired.

## Watch-outs
- Plan for downtime.
- Key gaps to flag to stakeholders: multiple subscriptions not supported; DR not available in NMM; App Attach incompatible with Azure AD DS.

*Bron: Nerdio-content 'Migrating from NME to NMM' (Blogs).*

## Verwante notities

- [Why Nerdio built a multi-tenant MSP product on top of split-tenant NMW](nerdio-manager-for-msp-why-multi-tenant.md)
- [Moving images and AVD objects from NME to NMM via Azure tags](nerdio-nme-to-nmm-image-migration-via-tags.md)
- [NME and NMM are hardened differently; don't copy one onto the other](nme-and-nmm-harden-differently.md)
- [NMM architecture: native Azure PaaS deployed into the MSP's own tenant](nmm-architecture-paas-in-msp-tenant.md)
- [NMM's four customer onboarding scenarios and what each reuses](nmm-customer-deployment-scenarios.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [Migrating WVD from Tenant to Workspace (ARM) in Nerdio](wvd-tenant-to-workspace-arm-migration.md)
