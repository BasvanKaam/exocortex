---
type: positie
merk: bvk
domein: ai-tooling
status: actief
datum: 2026-10-02
tags: [positie, ai, agents, failover, resilience, model-router, governance]
bron: linkedin-nieuwsbrief
---

# The model under your agent is a dependency that can disappear

After Claude Fable 5 was pulled worldwide three days after launch (June 2026), Bas's takeaway was not political but architectural: the model under an agent is a dependency with a failure mode EUC never had on the list. Not an outage or a deprecation with a runway, but a regulatory switch that fires for everyone at once, with no notice and no date for when it lifts.

## What follows
- Know which of your agents would stop tomorrow if their model went away.
- Couple agent and model loosely, so losing a model is a config change, not a rebuild.
- Have a fallback that is already wired and tested, not one you will build when you need it. A different model behaves differently, so test it rather than assume it.
- Tools exist (Foundry model router, failover in your own code) but were built for wobbly endpoints; they only help if another model can actually carry the work.
- Govern the model as an asset, next to the agent's identity, scope and logs. Its availability is not fully in your hands, or even the vendor's.

## Tone
He explicitly refused to pick a side between the government and Anthropic: "the facts are still moving and part of it is not public." Lay both views next to each other, then go to what matters for the reader's work.

*Bron: LinkedIn newsletter, Fable 5 edition (June 2026).*

## Verwante notities

- [Newsletter: The model under your agent can disappear (Fable 5)](bron-nieuwsbrief-2026-fable-5-pulled.md)
- [Build model-agnostic, the model is part of your supply chain](positie-build-model-agnostic.md)
- [Define what an agent outcome is worth before you open a dashboard](positie-define-agent-value-before-the-dashboard.md)
