---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [zero-trust, identity, conditional-access, rbac, avd, windows-365, cheat-sheet, dated]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Zero Trust Identity Controls in Nerdio (AVD + W365)

Cheat-sheet mapping of Zero Trust identity verification to concrete controls available in/around Nerdio for AVD and Windows 365. Companion to a basvankaam.com blog post (which adds ping-test and latency details).

## Identity verification
- Enforce MFA across both AVD and Windows 365.
- Conditional Access policies; use Entra ID + Conditional Access to block risky logins automatically.
- Contextual / adaptive authentication based on device, location, and risk. Enforce adaptive access controls on every session launch, even via Intune.
- Biometrics support.

## Authentication methods
- Supports Entra ID, AD DS, Entra DS, and Hybrid Join, to meet varied compliance and hybrid identity scenarios. Combine identity strategies with dedicated join accounts and scoped roles.

## Dedicated join account
- Least-privilege AD join accounts per pool, with OU separation.

## Access governance
- Nerdio RBAC: built-in plus custom roles. Role templates for AVD Admin, Desktop Admin, Helpdesk, etc.
- PIM (Azure AD / Entra) for time-based access elevation.

The through-line: layer identity, scoped roles, and just-in-time elevation rather than relying on a single control.

*Bron: Nerdio-content 'Zero Trust Cheat Sheet' ((root)).*

## Verwante notities

- [AVD Security Checklist by Layer (Bas's Cheat Sheet)](avd-security-checklist-by-layer.md)
- [Delegated vs Application Permissions (Microsoft Graph)](delegated-vs-application-permissions-graph.md)
- [Mapping Zero Trust Principles to Real NME Capabilities](mapping-zero-trust-to-nme-capabilities.md)
- [Zero Trust extras: patching cadence and CIS-hardened images](zero-trust-hardening-extras-patch-cis-images.md)
- [Zero Trust principles mapped to AVD and Windows 365 in NME](zero-trust-mapped-to-avd-w365-nme.md)
- [Zero Trust Security Model](zero-trust-model.md)
