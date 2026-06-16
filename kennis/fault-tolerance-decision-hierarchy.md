---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [high-availability, resilience, principles, clustering, virtualization, consulting-tool]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Fault-Tolerance Decision Hierarchy (Application HA Before Hypervisor HA)

A decision rule Bas applies when designing availability for a critical environment. The ordering is deliberate, not arbitrary:

1. **Use the application's own fault-tolerance first.** Where the application supports high availability natively, use that.
2. **Fall back to the virtualization (hypervisor) layer** only where the application does not support HA itself.

Supporting rules that travel with it:

- HA is applied to every component critical to keeping the core platform and business-critical processes running. In practice that means at least two servers with the same role/function; each member is a *node*, the set is a *cluster*.
- Because the physical hardware is itself redundant, cluster nodes are deliberately *spread across different physical hosts* (anti-affinity), so a single hardware failure cannot take down a whole cluster.
- Availability is expressed as a contractual figure (e.g. 99.8%) and explicitly stated to be *exclusive of the maintenance window* - patching/updates happen inside a defined window that does not count against the SLA.
- Don't adopt a newer technique just because it is better on paper. In one design a newer storage-replication technology was documented as a genuinely stronger alternative to the established one, but explicitly *not chosen* because the investment time to validate it fell outside the project scope. The established, proven technology won. Note unchosen alternatives and *why* in the design.

The generalizable consulting move: choose the highest-fitness layer for resilience (closest to the application), make redundancy physically real (spread nodes), carve out maintenance from the SLA, and prefer proven over novel unless the project can afford to validate the novel.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a public-safety / emergency-services organization (shared emergency control-room consolidation)).*

## Verwante notities

- [Azure high-availability building blocks](azure-high-availability-building-blocks.md)
- [Design for Restore, Not Backup (RPO/RTO/MTPD First)](design-for-restore-not-backup.md)
- [On over-engineering HA: simplicity often wins, but it all depends](ha-it-all-depends.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
- [Restore Testing Cadence and Procedure](restore-testing-cadence.md)
- [Standardize-Then-Deviate Server Provisioning](standardize-then-deviate-provisioning.md)
- [Two-scenario advice and recommendation principles](two-scenario-advice-and-recommendation-principles.md)
