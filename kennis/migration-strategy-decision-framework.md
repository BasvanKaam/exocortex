---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [migration, besliskader, big-bang, fasering, active-directory, fall-back]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Migration strategy framework: transition vs transformation, big-bang vs phased, build-clean-alongside

The decision framework I apply when choosing how to move services onto a new platform. I make the choice explicit and write down the alternatives with their pros and cons, so the client owns the trade-off rather than inheriting my preference silently.

## First distinction: transition or transformation?
- **Transition** = take over the existing services as-is (lift the operations).
- **Transformation** = rebuild the services on the target platform and move into them.
If the analysis shows there is effectively nothing worth taking over as-is, I say so and drop the word "transition" entirely for the rest of the document. Naming this up front stops a lot of scope confusion later.

## Second distinction: big-bang or phased?
I list both and decide on risk:
- **Big bang** (everything over in one long weekend). Pro: no mixed old/new period, clearer for users. Con: huge pressure in one window, harder fall-back.
- **Phased / step-wise**. Pro: migration risk spread over time, simple per-step fall-back. Con: both organizations stay active on the migration for longer.
My default is **phased**, to keep the chance of things going wrong as low as possible. I migrate functions that are tightly coupled or interdependent **together**.

## Build clean alongside, then cut over
My preferred pattern for the identity/platform layer: build a **new, clean target** (e.g. a fresh single-forest/single-domain directory under provider best practice) **independently of and beside** the existing environment, rather than transforming the old one in place. Benefits I cite:
- Each party owns exactly one environment (clear ownership, no shared-responsibility mess).
- The new structure is clean, without legacy objects and legacy debt.
- The old environment's stability is never at risk during the build.
During the phased cut-over I create **temporary trusts/couplings** between old and new so not-yet-migrated apps and data stay reachable, and tear them down when done. The old environment stays available as **fall-back** for a defined period after migration.

## Data migration: sync over copy
For file data I prefer **continuous synchronisation per share** up to the cut-over moment over a one-shot big-bang copy: users keep working on the old share until that service's cut-over, then a per-share switch redirects them. This lets me migrate share by share, aligned to the service phasing.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a government ICT shared-service center onboarding a public-sector research/policy institute).*

## Verwante notities

- [Bas: The 6 R's for Application Rationalization](bas-6-rs-cloud-migration.md)
- [Cloud inventory method: joint assessment, waves, and the R's](cloud-inventarisatie-methode-waves-en-rs.md)
- [Migrate vs Modernize as a Per-Workload Decision](migrate-vs-modernize-distinction.md)
- [Position: phase the rollout and keep part of the legacy estate intact](position-phased-rollout-keep-legacy-intact.md)
- [Start small, test, then scale — because it de-risks the client's investment](position-start-small-test-then-scale-derisks-investment.md)
- [The 6 Rs of cloud migration](six-rs-cloud-migration-strategies.md)
- [Principles I apply on transformation engagements](transformation-principles-positions.md)
- [Transition/transformation engagement structure: intake, analyse, execute in plateaus](transition-transformation-engagement-structure.md)
