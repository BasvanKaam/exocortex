---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [zero-trust, security, avd, windows-365, nme, conditional-access, rbac, nerdiocon]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Zero Trust principles mapped to AVD and Windows 365 in NME

Bas's NerdioCon framework that takes the standard ten Zero Trust principles and shows, principle by principle, how each is implemented for Azure Virtual Desktop (AVD) and Windows 365 (W365) when managed by Nerdio Manager for Enterprise (NME). The framing line is "Zero Trust, a state of mind" - it is a posture, not a product you buy.

1. **Verify explicitly** - enforce MFA for AVD and W365 users via Entra ID (Azure AD) Conditional Access, integrated with NME's access policies.
2. **Use least privilege access** - define role-based access control (RBAC) in NME for admins so they get minimal permissions to manage AVD and W365; apply Just-in-Time (JIT) access for privileged users.
3. **Assume breach** - enable session-based monitoring and risk-based access policies; use session shadowing and anomaly detection via security alerts.
4. **Enforce device health and compliance** - use NME-driven compliance policies so only healthy, compliant AVD/W365 sessions can be established; back with Azure AD compliance policies where needed.
5. **Secure access to applications and data** - combine NME access controls with Conditional Access for context-based security (deny risky locations, force MFA for sensitive apps).
6. **Monitor and log all activity** - use NME security dashboards for user activity, session analytics, and compliance adherence across AVD and W365.
7. **Network and micro-segmentation** - segment access per user group via AVD host pools in NME; use VNet segregation to restrict lateral movement.
8. **Automate threat detection and response** - automate session-based policies to disable non-compliant sessions; integrate Microsoft Defender for Endpoint to isolate risky connections.
9. **Apply encryption everywhere** - BitLocker on W365 Cloud PCs; enforce TLS for AVD session traffic via NME policy controls.
10. **Zero Trust mindset across the org** - reinforce with role-specific training, because users are the weakest link; use NME for real-time insight and compliance reporting.

Dated: tied to NME feature set and product naming (Azure AD / Entra ID transition) as of early 2025; verify each control against current NME Help before reuse.

*Bron: Nerdio-content 'NC Zero Trust notes' (NerdioCon).*

## Verwante notities

- [AVD Security Checklist by Layer (Bas's Cheat Sheet)](avd-security-checklist-by-layer.md)
- [Mapping Zero Trust Principles to Real NME Capabilities](mapping-zero-trust-to-nme-capabilities.md)
- [Generic security awareness fails; training must be role-based](position-security-awareness-must-be-role-based.md)
- [Zero Trust Identity Controls in Nerdio (AVD + W365)](zero-trust-controls-nerdio-avd-w365.md)
- [Zero Trust extras: patching cadence and CIS-hardened images](zero-trust-hardening-extras-patch-cis-images.md)
- [Zero Trust Principles](zero-trust-principles.md)
- [Zero Trust session method: lead with the weakest link](zero-trust-session-method-weakest-link.md)
