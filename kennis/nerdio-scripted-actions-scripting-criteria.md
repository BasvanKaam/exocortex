---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, scripted-actions, powershell, avd, wvd, automation, variables]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Nerdio Scripted Actions: scripting criteria & predefined variables

The technical contract a scripted action must satisfy to run inside Nerdio Manager, plus the variables Nerdio passes in. Captured from the 2021 Hackathon brief (WVD/Classic era; variable set and product naming are dated).

## Execution criteria
- Scripted actions must be able to run under the **local system account**.
- AD credentials can be passed in via variables. Nerdio Manager (WVD and MSP) does this automatically.
- Scripts do not have to be Nerdio-specific; they should run against native Azure objects too (host pools, Azure images, MSIX App Attach, Azure Files, FSLogix, various OSes and VMs).
- You start the process with PowerShell, but PowerShell can spawn other tooling: run everything natively in PowerShell, or use it to kick off ARM templates, Bicep, Packer, etc. Scripts may reference other scripts.

## Predefined variables Nerdio passes to a script
WVD ARM:
- $HostPoolId
- $HostPoolName

WVD Classic:
- $TenantGroupName
- $TenantName
- $HostPoolName

All:
- $AzureSubscriptionId
- $AzureSubscriptionName
- $AzureResourceGroupName
- $AzureRegionName
- $AzureVMName
- $ADUsername (if passing AD credentials)
- $ADPassword (if passing AD credentials)
- $DesktopUser (if using with a personal host pool)

Note: this reflects the WVD ARM / WVD Classic split of that era; verify the current variable set against Nerdio's live docs before reuse.

*Bron: Nerdio-content 'Hackathon overview doc.docx' (Hackathon).*

## Verwante notities

- [Idea: Nerdio vs shadow IT](idee-nerdio-shadow-it-governance.md)
- [Idea: The self-healing MSP environment](idee-self-healing-msp-environment.md)
- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
- [PowerShell: download the latest release asset from GitHub](powershell-download-latest-github-release.md)
