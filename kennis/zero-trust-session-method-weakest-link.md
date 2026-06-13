---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [idee, instructional-method, security-awareness, role-based-training, session-design, nerdiocon]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# Zero Trust session method: lead with the weakest link

Bas's reusable instructional structure for a 45-minute security session, designed so the technical control mapping does not dominate. The throughline: technology mapping first, then pivot to the human, because the end user is the biggest risk.

Session arc (45 min):
1. Introduction - the urgency: evolving threat landscape in virtual desktops, why AVD and W365 specifically need Zero Trust, key risks (session hijacking, unsecured RDP, weak user policies).
2. Enforcing TLS encryption - why it matters (stops man-in-the-middle and RDP exploits), how to enforce via NME settings, NSGs, and Azure Firewall, with a live demo of TLS 1.2+ and blocking legacy RDP.
3. Policy-driven security in NME - RBAC and Conditional Access, automating session security and compliance, risk-based authentication, live demo.
4. The weakest link: end-user behaviour - why users are the biggest risk, common mistakes, why phishing and social engineering still work, run a live simulation: "How easily can we trick an end-user?"
5. Role-based security training - the core argument: awareness must be job-specific, not generic. Build separate tracks for IT admins vs finance vs HR vs sales, delivered as security micro-trainings.
6. Q&A and final takeaways with concrete action items.

Reusable method elements (channel-agnostic): open with urgency and concrete risks; alternate explanation with live demos; insert a live interactive simulation ("The Weakest Link") so the audience feels the human risk instead of hearing about it; close every section with practical action items, not theory.

*Bron: Nerdio-content 'NC Zero Trust notes' (NerdioCon).*

## Verwante notities

- [ADDIE Method: Designing a Step-by-Step Hardening Training](addie-method-hardening-training-design.md)
- [Lead enablement with hands-on labs, not slideware](hands-on-labs-over-slideware.md)
- [Method: The Learning Pyramid Applied to Technical Training](learning-pyramid-training-method.md)
- [Generic security awareness fails; training must be role-based](position-security-awareness-must-be-role-based.md)
- [Zero Trust extras: patching cadence and CIS-hardened images](zero-trust-hardening-extras-patch-cis-images.md)
- [Zero Trust principles mapped to AVD and Windows 365 in NME](zero-trust-mapped-to-avd-w365-nme.md)
