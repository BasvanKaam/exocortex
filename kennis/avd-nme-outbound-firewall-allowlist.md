---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, nme, firewall, outbound, session-host, networking]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# AVD / NME outbound firewall allow-list

When session-host VMs or the vNet-integrated NME app have restricted egress (custom routing, NSGs, proxy/GPO), these outbound destinations must be reachable for AVD + NME to work.

## Session host outbound (port / purpose / service tag)
- `login.microsoftonline.com` 443 – Microsoft Online auth
- `nmwextensions.blob.core.windows.net` 443 – Nerdio DSC extension
- `*.wvd.microsoft.com` 443 – AVD service traffic (WindowsVirtualDesktop)
- `*.prod.warm.ingest.monitor.core.windows.net` 443 – agent traffic (AzureCloud)
- `catalogartifact.azureedge.net` 443 – Azure Marketplace (AzureFrontDoor.Frontend)
- `gcs.prod.monitoring.core.windows.net` 443 – agent traffic
- `kms.core.windows.net` / `azkms.core.windows.net` 1688 – Windows activation
- `mrsglobalsteus2prod.blob.core.windows.net` 443 – agent and SxS stack updates
- `wvdportalstorageblob.blob.core.windows.net` 443 – Azure Portal support
- `169.254.169.254` 80 – Azure Instance Metadata Service
- `168.63.129.16` 80 – session host health monitoring
- `oneocsp.microsoft.com` / `www.microsoft.com` 80 – certificates

## NME app vNet-integration outbound (extra)
- `nwp-web-app.azurewebsites.net` 443 – Nerdio licensing servers
- Azure SQL 1433 + 11000-11999 (AzureSQL service tag)
- `*.applicationinsights.azure.com` 443 – Application Insights
- `login.microsoftonline.com` / `graph.microsoft.com` 443 – authentication (AzureIdentity)
- `login.windows.net` 443 – AAD SQL authentication
- `management.azure.com` 443 – AVD management
- `api.github.com` / `*.githubusercontent.com` 443 – scripted-actions repository / content
- `[KeyVaultName].vault.azure.net` (or `*.vault.azure.net`) 443 – Key Vault access
- `api.loganalytics.io` / `api.applicationinsights.io` 443 – Log Analytics / App Insights API

Note: Microsoft has retired older agent URLs; allow the new `*.prod.warm.ingest.monitor.core.windows.net` and remove deprecated endpoints. Adjust outbound rules for inline scripts when using Inline Execution Mode without a Hybrid Worker.

*Bron: Nerdio-content 'Hardening Nerdio Manager for Enterprise Services v1.0' (Training).*
