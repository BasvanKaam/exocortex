---
type: positie
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [positie, backup, restore, rpo-rto, business-continuity, design-principle, consulting-tool]
bron: salomon-opdrachten
---

# Design for Restore, Not Backup (RPO/RTO/MTPD First)

Bas's stated position when designing a backup solution: the point is not the backup, it is being able to *correctly restore* the data. So the design starts from the restore requirement, not from a backup product or schedule.

The method:

- First establish what data actually has to be restorable and how critical it is. That requirement is the input for the backup strategy, not the other way around.
- Quantify it with three explicit metrics, defined per application:
  - **RPO (Recovery Point Objective)** - how much data are you willing to lose? (e.g. for critical voice-logging the answer was: zero recordings may be lost.)
  - **RTO (Recovery Time Objective)** - within what time must the application be available again after unplanned downtime?
  - **MTPD (Maximum Tolerable Period of Disruption)** - how long a disruption the organization tolerates at all.
- Translate vague client demands into precise, testable requirements. Example of his sharpening: a client demand that "everything must be backed up immediately" is reformulated as *open files are not expected to be backed up; the moment a file is closed it must be backed up immediately, and loss of an open file that corrupts is accepted*. This removes the impossible interpretation and leaves an implementable rule.
- Because daily change rate is usually unknown up front, set the backup strategy in stages: install/initialize, measure the change rate with monitoring, then design the real strategy on the measured data rather than guessing.

The principle generalizes: continuity design is requirements-driven (what must survive, at what cost, recoverable in what window), and the consultant's job is to convert fuzzy availability wishes into RPO/RTO/MTPD figures that drive every downstream choice.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a public-safety / emergency-services organization (shared emergency control-room consolidation)).*

## Verwante notities

- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [Fault-Tolerance Decision Hierarchy (Application HA Before Hypervisor HA)](fault-tolerance-decision-hierarchy.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [Why high availability and DR matter: ransomware and data hostage](ransomware-data-hostage.md)
- [Restore Testing Cadence and Procedure](restore-testing-cadence.md)
- [SLA availability to allowed-downtime reference (the nines)](sla-availability-nines-downtime-table.md)
