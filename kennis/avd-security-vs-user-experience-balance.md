---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, security, user-experience, positie]
bron: nerdio-blog
---

# Security is always a fine line against user experience

Bas's recurring stance across the AVD security cheat sheet: every lockdown measure is a trade-off between user productivity and overall security, and finding the right balance is the hard part but worth the effort. He repeats this explicitly around session time limits, machine inactivity limits, screen lock, and device redirection: consider the pros and cons before implementing, do not just switch everything on. He pairs the security argument with a cost argument: Nerdio autoscale can shut down or remove idle machines so they are not exposed and not costing resources.

A second stance: he frames the sheet as a starting point, not a mandate. On patching he is explicit: "We are not the ones telling you how and when to do it; we provide the tools." The vendor supplies tooling and consistency, the customer owns the strategy.

A third, smaller stance on proxies: bypass proxies for AVD traffic. Proxies do not make AVD more secure (traffic is already encrypted) and they add latency and packet loss; route AVD around the proxy if policy requires one for general web traffic.

*Bron: Nerdio-content 'Azure Virtual Desktop Security Guidelines Cheat Sheet - v2.0' (Blogs).*

## Verwante notities

- [AVD security cheat sheet: the six-category framework](avd-security-cheat-sheet-framework.md)
- [AVD Security cheat sheet v2.0 — 44 best practices](avd-security-cheat-sheet-v2.md)
- [AVD Security Checklist by Layer (Bas's Cheat Sheet)](avd-security-checklist-by-layer.md)
- [Don't leave desktop power management to users alone](dont-leave-power-management-to-users.md)
- [Harden step by step and verify between steps, don't lock everything at once](harden-step-by-step-not-all-at-once.md)
- [Involve and educate users early or adoption fails](involve-users-early-for-adoption.md)
- [Cost Saving Shouldn't Be the Main Reason to Go Cloud](positie-cost-savings-not-the-main-reason.md)
- [Generic security awareness fails; training must be role-based](position-security-awareness-must-be-role-based.md)
- [Frame security guidance as a living starting point, not a final word](security-checklist-as-living-starting-point.md)
