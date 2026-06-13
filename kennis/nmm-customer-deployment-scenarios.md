---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmm, msp, wvd, deployment, onboarding]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# NMM's four customer onboarding scenarios and what each reuses

After installing NMM (about 30-45 minutes from the Azure marketplace), onboarding customers follows one of four wizard-driven, largely automated scenarios. The pattern: NMM provisions whatever identity/network/storage is missing, reuses whatever already exists, then always builds a full WVD environment on top.

- Greenfield (60 minutes or less): no Azure footprint. NMM creates an all-PaaS environment - Azure AD Domain Services, then a VNet, then the domain and an Azure Files-based file share, then a full WVD deployment (workspace, one or more host pools, VM hosts).
- Landing zone (30 minutes or less): existing traditional AD or Azure AD Domain Services already in place. NMM leverages the existing identity provider, reuses existing resource groups and networks, provisions a new Azure Files share, then builds the WVD environment.
- Existing IaaS (10 minutes or less): groundwork for Azure VMs/WVD hosts mostly in place. NMM reuses the existing identity provider, VNet and file storage, then builds the WVD environment.
- Existing WVD (10 minutes or less): NMM acts as a direct overlay on top of an existing WVD environment plus its identity, networking, file storage and resource groups, adding its management/optimization layer within minutes.

What NMM then adds across scenarios: per-user Azure cost reporting, a wizard-driven cost estimator, best-practice/performance recommendations, image management for WVD hosts, application management, MSIX AppAttach, FSLogix Profile Containers, backups, user/session/Azure AD group management, easy VM resizing/scheduling (e.g. D-series to B-series at night, or off overnight and on in the morning), and the built-in autoscaling engine carried over from NMW. Single-session and multi-user are both supported.

*Bron: Nerdio-content 'Nerdio Manager for MSP - Customer deployment scenarios_final' (Blogs).*

## Verwante notities

- [Moving images and AVD objects from NME to NMM via Azure tags](nerdio-nme-to-nmm-image-migration-via-tags.md)
- [NME to NMM migration runbook (AVD)](nme-to-nmm-migration-runbook.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
