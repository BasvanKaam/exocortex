---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [w365, cloud-pc, cost, licensing, nerdio, dated]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Windows 365 License Optimization: The Three Levers

Because Windows 365 is licensed per user per month (not metered like AVD), the cost game is about not paying for licenses nobody is using. Bas's reusable framing breaks it into three levers, with the why behind each.

## 1. Auto-assignment (don't pay until first sign-in)
Assign a license only when a user signs in for the first time (via a browser, using a published first-sign-in URL). Users who never sign in never consume a license. Saves on the gap between "licensed on paper" and "actually used."

## 2. Unused-license reclamation
Reclaim licenses from users who haven't signed in for a defined period (left the org, changed habits). The user is removed from the licensed group, their Cloud PC enters a 7-day grace period, then is removed. Reclaimed licenses get reused or cancelled.

## 3. Inactive-user license parking
Users are actively connected only ~40-50 hours/week, so a Cloud PC is not used 24/7. When a user is signed off, park them on a cheaper license; reassign the original on next sign-in. Key compliance nuance: you cannot leave a user with no license at all, so a minimal "parking" license is required to stay compliant. Parking does not resize the VM, it only swaps the license temporarily. (Windows 365 license changes are exempt from the short-term reassignment restrictions that apply to other M365 products.)

## Why it matters
The levers exist because of the fixed-per-user model: the only way to optimize spend is to minimize the count of assigned/active licenses while staying license-compliant.

*Bron: Nerdio-content 'w365 Cloud PC - getting started' ((root)).*

## Verwante notities

- [Always-on Cloud PCs are wrong for intermittent users; Frontline fills the gap](choose-frontline-vs-enterprise-cloud-pc.md)
- [Cloud PC licensing requirements (durable)](cloud-pc-licensing-requirements.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-added-value-on-cloud-pc.md)
- [Nerdio non-technical cost levers](nerdio-non-technical-cost-levers.md)
- [Windows 365 Cloud PC: What It Is and How It Differs from AVD](w365-cloud-pc-vs-avd-fundamentals.md)
- [Windows 365 Frontline: concurrency licensing for shift/frontline workers](windows-365-frontline-concurrency-model.md)
