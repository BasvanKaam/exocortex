---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, security, zero-trust, nerdio, cheat-sheet, conditional-access, defender]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# AVD Security Checklist by Layer (Bas's Cheat Sheet)

Bas's reusable way to structure an AVD security review: start with Microsoft Secure Score, layer controls bottom-up, and always answer "who is responsible for what?" first.

## Identity & access layer
- Entra/Azure AD MFA for all VDI logins.
- Conditional access: geo-location based, hybrid-AD device based, plus sign-in-risk and user-risk policies (block suspicious / TOR IPs).
- Azure Policy to allow only required resources in the subscription (e.g. block public IPs, restrict VM SKUs).

## Network layer
- Control all ingress/egress: Windows Firewall, Azure NSGs, hub firewall, proxy servers.
- Separate production / non-production VDI by subnet, inter-subnet communication denied by default.
- Prefer **private endpoints** over service endpoints.
- Never expose a machine directly to the internet; avoid direct RDP to session hosts.

## OS & machine layer
- Patch strategy, session time limits, screen lock for idle sessions.
- Control device redirection per host pool (printers, local/USB drives, clipboard, screenshots, camera).
- OS disk encryption; onboard to Microsoft Defender for Endpoint (EDR) and scan regularly, or a third party. Exclude the VHD extension when using FSLogix.
- DLP to prevent data loss; watermarking for privacy; AppLocker / Defender Application Control to block unauthorized software.
- Use separate service accounts for admin activity, not normal user IDs.
- Trusted Launch on Gen 2 VMs (Secure Boot, vTPM); limit local install permissions (consider a sandbox).

## Supporting controls
- Cloud Policy Service (M365 Apps Admin Center, also reachable via Intune 'Policies for Office Apps') for M365 app security policies across Windows/iOS/Android; user policies only, includes Security Baselines, no template downloads needed.
- Azure Management Groups to apply governance/compliance above the subscription level (subscriptions inherit conditions).
- Confidential VMs, EU Data Boundary for Azure, zero-trust principle as guiding frames.

*Bron: Nerdio-content 'Nerdio - AVD security cheat sheet' (Blogs).*

## Verwante notities

- [AVD security cheat sheet: the six-category framework](avd-security-cheat-sheet-framework.md)
- [AVD Security cheat sheet v2.0 — 44 best practices](avd-security-cheat-sheet-v2.md)
- [Security is always a fine line against user experience](avd-security-vs-user-experience-balance.md)
- [AVD Shared Responsibility: Who Secures What](avd-shared-responsibility-model.md)
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [Zero Trust Identity Controls in Nerdio (AVD + W365)](zero-trust-controls-nerdio-avd-w365.md)
- [Zero Trust extras: patching cadence and CIS-hardened images](zero-trust-hardening-extras-patch-cis-images.md)
- [Zero Trust principles mapped to AVD and Windows 365 in NME](zero-trust-mapped-to-avd-w365-nme.md)
