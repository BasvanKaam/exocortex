---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [hardening, method, security, positie, nme]
bron: nerdio-training
---

# Harden step by step and verify between steps, don't lock everything at once

My argument throughout the NME hardening module: hardening is an iterative process, not a switch. Each lockdown step (private endpoint, DNS, disable public access) must be applied and then verified before the next, otherwise when something breaks you can't tell which change caused it. That's also why I prefer (or at least respect) the manual route over the automated runbook in learning contexts: an explicit advantage of doing it by hand is you can confirm NME still works in between steps, taking a granular, controlled approach. Hardening is also never a one-time task; it's ongoing, adapting to evolving threats and business needs.

And a stance on timing: hardening belongs in the post-sales / PoV phase, not the 30-day trial. The trial is for evaluating core functionality and ease of management fast; full security hardening is customer-specific, needs multiple teams to agree, and routinely takes longer than 30 days. Prioritise usability in the trial, defer deep hardening, with exceptions where warranted.

*Bron: Nerdio-content 'Hardening Nerdio Manager for Enterprise Services v1.0' (Training).*

## Verwante notities

- [AVD / NME outbound firewall allow-list](avd-nme-outbound-firewall-allowlist.md)
- [Security is always a fine line against user experience](avd-security-vs-user-experience-balance.md)
- [Hardening Nerdio and AVD: Easy Way vs Hard Way](hardening-nerdio-avd-easy-vs-hard.md)
- [Always Test Before Revoking API Permissions](positie-test-before-revoking-api-permissions.md)
