---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [consulting, advice, scenarios, principles, risk, fasering, positie]
bron: salomon-opdrachten
---

# Two-scenario advice and recommendation principles

My stance on how to give infrastructure advice that a client can actually act on with low regret.

## Always two scenarios, one a derivative of the other
I work out two scenarios, not one and not five. The second is deliberately a split-off of the first: it reuses most of the same building blocks and only the genuinely different parts are re-described in detail; everything unchanged is marked as such. This keeps the choice legible. Example from practice: scenario 1 is a shared virtual-desktop-heavy approach; scenario 2 shifts to managed laptops with a smaller central environment (the virtual-desktop host count dropped from eight to three), but reuses the same profile, file, backup, MFA, identity and management stack.

## Recommendation principles
- **Start small, test, then scale.** In all cases begin small and test thoroughly before the next step. This minimizes the client's investment risk. The indicative monthly/annual cost applies to a fully delivered environment; the first months cost a fraction of that.
- **Match the billing model to the phase.** Use pay-as-you-go during the test phase (per-unit it is more expensive, but few machines and the ability to switch things off keeps spend minimal and gives easy scale up/down). Move to reserved instances (1 or 3 year) once the design is fixed; in this engagement that was roughly a 40% saving versus pay-as-you-go.
- **Keep it as small, simple and cheap as possible.** Prefer native platform capabilities first; only reach for a third-party partner solution when it is clearly demonstrated that you cannot do without it. Note partner options, but do not default to them.
- **Scale out, not just up, for resilience.** Prefer several smaller hosts over one large one so a single-machine failure has limited blast radius.
- **Weigh cost against benefit explicitly, and say no when it does not pay off.** When a client wants something (e.g. taking full account-management control in-house) that needs heavy infra and organizational change for minimal return, I say so plainly: the costs do not outweigh the benefits, here is the cheaper alternative (renew the SLA arrangement instead).
- **No guarantees, no invented certainty.** State that the advice is expected to meet the requirements but cannot be guaranteed; prices and products change. Flag anything that still needs testing or further research rather than asserting it.
- **Surface downstream consequences.** Big infrastructure and data-location changes ripple into audits, certifications and compliance; call that out as needing separate attention.

## Related
- Engagement structure: workplace and infrastructure assessment
- IST/SOLL report skeleton
- Cloud-migration suitability checklist for client/server applications

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (property and real-estate services organization (multi-entity, multi-site)).*

## Verwante notities

- [Advice report structure: current-state and advice mirror the same layers](advice-report-structure-current-state-mirrors-advice.md)
- [Engagement structure: workplace and infrastructure assessment](engagement-structure-workplace-infra-assessment.md)
- [Fault-Tolerance Decision Hierarchy (Application HA Before Hypervisor HA)](fault-tolerance-decision-hierarchy.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [IST/SOLL report skeleton](ist-soll-report-skeleton.md)
- [Start small, test, then scale — because it de-risks the client's investment](position-start-small-test-then-scale-derisks-investment.md)
- [Standardize-Then-Deviate Server Provisioning](standardize-then-deviate-provisioning.md)
- [The Two-Scenario Offer: Centralized Backend vs Managed-Laptop-Only](two-scenario-offer-pattern.md)
