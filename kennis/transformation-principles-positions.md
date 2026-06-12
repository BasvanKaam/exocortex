---
type: positie
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [positie, principes, standaardisatie, verantwoordelijkheid, security-by-design, never-invent]
bron: salomon-opdrachten
---

# Principles I apply on transformation engagements

Positions I hold and apply when moving an organization onto a managed/shared platform. These are the calls I make by default and defend.

## Standardisation before differentiation
Lead with standard building blocks; allow client-specific solutions only where genuinely needed, and be explicit that they are **less cost-effective and less flexible**. A standard catalogue of building blocks beats bespoke almost every time. Where the legacy estate split things for purely technical reasons, I do not blindly reproduce that split on the new platform.

## Clean rebuild over lift-and-shift
Given the choice, I build a clean new target beside the old one and migrate into it, rather than dragging legacy structure and objects forward. A clean directory/structure is worth the extra client effort of supplying good data.

## Hard demarcation of responsibility
No shared responsibility inside one production line. Either the provider does technical management of an application/site or the client does — never mixed on the same servers. The provider owns infrastructure; the client keeps **functional management** of its own applications and data. Clear ownership per environment prevents the finger-pointing that kills these programmes.

## Skip the lift-and-shift of incidents
The provider does **not** take over existing open calls/incidents during transformation, and does not run the client's old environment. Clean start on operations.

## Freeze before cut-over
Agree a **freeze period** (e.g. two weeks) before each transformation moment: no technical changes on the source environment that could impact the move. And get joint sign-off on the test & acceptance plan before executing.

## Client decides risk acceptance; I advise
Where a security/usage choice is the client's to make (e.g. allowing personal USB storage), I make the decision theirs explicitly and record my **advice** alongside it. Security is treated as integral and by-design, not bolted on; specific services follow the baseline, and any deviation is described and signed off by the client's authority.

## Verify, don't assume
I mark client-supplied data as unverified when it is, re-verify analysis-phase information against current reality at the start of execution, and re-inventory estimated counts before they become commitments. Never present an unchecked number as fact.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a government ICT shared-service center onboarding a public-sector research/policy institute).*

## Verwante notities

- [Positions I apply in a cloud transition](cloud-transitie-posities.md)
- [Engagement Preconditions Are a Risk-Transfer Contract](engagement-preconditions-are-risk-transfer.md)
- [Migration strategy framework: transition vs transformation, big-bang vs phased, build-clean-alongside](migration-strategy-decision-framework.md)
- [Start small, test, then scale — because it de-risks the client's investment](position-start-small-test-then-scale-derisks-investment.md)
- [Standardize-Then-Deviate Server Provisioning](standardize-then-deviate-provisioning.md)
- [Transition/transformation engagement structure: intake, analyse, execute in plateaus](transition-transformation-engagement-structure.md)
