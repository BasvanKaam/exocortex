---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nme, hybrid-worker, azure-automation, scripted-actions, runbooks]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# NME hybrid worker vs inline-script runbook execution

## What a Hybrid Worker is
A VM (a Server 2022 Datacenter machine works) that runs Azure Automation jobs **locally inside a private vNet** instead of in Azure's cloud sandbox. It registers with an Automation Account, listens for jobs, executes them locally and returns logs/results to Azure Automation. NME relies on Automation Accounts for scripted actions: deploying AVD hosts, custom scripts, VM maintenance, software install/updates.

## When you still need one
When you harden the environment (e.g. make the Scripted Actions Storage Account private) and private endpoints block Azure's default cloud automation from reaching SQL/Key Vault/Storage/Automation. The trade-off: another VM to patch, secure and maintain, plus storage and compute cost.

## Inline Script Runbook Execution Mode (as of NME v7.1)
Lets Azure Runbooks execute securely in hardened environments **without a Hybrid Worker VM**, even when storage accounts are private. This is the preferred path now; the Hybrid Worker is only required when Inline Mode is not used, or for advanced isolation / compliance needs.

## The "Enable Private Endpoints" runbook
NME has a runbook that automates the hardening: checks/creates the vNet, configures the endpoint and app subnets, links private DNS zones, creates private endpoints for SQL/Key Vault/Storage/Automation/App Service, and optionally hardens the CSSA storage account (deploying a Hybrid Worker), peers vNets, and enables Private Link for Azure Monitor. Faster and less error-prone than manual, but less flexible; the manual route lets you verify NME between each step.

## Newer hardened-environment features (NME v7.1+)
- **WinGet** supports automatic private endpoint configuration; NME creates private endpoints on the integrated vNet for its Web App, Key Vault, Cosmos Account and Storage Account.
- **Azure AI** features (PII detector, Auto-Scale Analytics recommendations) can run entirely over private endpoints on the integrated vNet.
- **Entra ID is the default SQL authentication method** for new installs, replacing traditional SQL auth.

## Pre-flight script
NME has a pre-deployment validation script (run locally on Windows/macOS/Linux or in Cloud Shell, ~10 min): it tries to create each required resource type (Log Analytics, Storage, SQL Server/DB, App Service Plan, Automation Account, Key Vault) and, if blocked, identifies the Azure Policy that's preventing it; it also checks resource-provider state and role assignments, then cleans up its test resources. Run this before install in policy-heavy tenants to avoid failed deployments.

*Bron: Nerdio-content 'Hardening Nerdio Manager for Enterprise Services v1.0' (Training).*

## Verwante notities

- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
