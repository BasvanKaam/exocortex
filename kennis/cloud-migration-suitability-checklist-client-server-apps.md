---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [consulting, cloud-migration, assessment, checklist, client-server, decision-framework, method]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Cloud-migration suitability checklist for client/server applications

A reusable decision framework I apply per application before deciding whether and how to move a client/server application to the cloud. The point is to inventory dependencies and requirements first, then let that determine the migration path and the VM/compute sizing, rather than guessing.

## Questions to answer per application
- Is the software, system or data latency-sensitive?
- Are there other network requirements?
- Where does the data live in the new (cloud) situation?
- May, and does the client want, all data to go to the cloud?
- How much data is it (per user / per department / other)?
- Specific storage requirements (block, file, system)?
- Dependencies on OS, system, dongle or other hardware?
- Dependencies on other applications or software?
- Is the software suitable/certified for multi-user use?
- Specific security requirements: encryption, authentication?
- What are the minimum or desired system requirements?
- Light, medium or heavy usage profile (memory, CPU, IOPS)?

## How the outcome is used
- The answers decide whether the system can move, by what method, and which VM type and compute (memory, CPU, storage, network) to pick.
- Compatibility with a newer OS is a first-class concern: test each app on the target server/desktop OS before committing, and write a dedicated test plan for it.
- Test how the app behaves (user experience) over a public internet connection, not just inside the old LAN.
- Watch for hard couplings to shared department drives (for example hard-coded UNC paths from applications into a file share); inventory these explicitly before re-platforming the data.
- Some applications are simply unsuitable for shared/published delivery (heavy graphics/CAD, certain finance suites); plan to install those locally and manage them remotely instead.

## Related
- IST/SOLL report skeleton
- Two-scenario advice and recommendation principles
- Engagement structure: workplace and infrastructure assessment

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (property and real-estate services organization (multi-entity, multi-site)).*

## Verwante notities

- [Moving 32-bit to 64-bit (and 2003 to 2008) means app-compat work (durable lesson)](32bit-to-64bit-app-compat-is-a-fact-of-life.md)
- [Bas: The 6 R's for Application Rationalization](bas-6-rs-cloud-migration.md)
- [Cloud inventory method: joint assessment, waves, and the R's](cloud-inventarisatie-methode-waves-en-rs.md)
- [Gate cloud eligibility on data classification, with CISO sign-off](data-classification-gates-cloud-eligibility.md)
- [Engagement structure: workplace and infrastructure assessment](engagement-structure-workplace-infra-assessment.md)
- [My intake method: per-service IST/SOLL gap analysis with MoSCoW and coverage scoring](intake-ist-soll-gap-analysis-method.md)
- [IST/SOLL report skeleton](ist-soll-report-skeleton.md)
- [Joint Inventory: Two Pairs of Eyes Beat One](joint-inventory-two-pairs-of-eyes.md)
