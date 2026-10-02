---
type: bron
merk: bvk
domein: ai-tooling
status: actief
datum: 2026-10-02
tags: [linkedin, nieuwsbrief, eucnewsnuggets, foundry, claude, agents, model-router, failover, export-control]
bron: linkedin-nieuwsbrief
---

# Newsletter: The model under your agent can disappear (Fable 5)

Analysis edition, mid June 2026, in the week after 12 June. Claude Fable 5 arrived in Microsoft Foundry, Foundry Agent Service and GitHub Copilot on 9 June; on 12 June a US export control directive suspended Fable 5 and Mythos 5 for foreign nationals, and Anthropic disabled both models for every customer to stay compliant. Bas deliberately does not pick a side; his question is what happens to the agent you built when its model disappears.

## Core points
- The odd in-between state: Foundry still listed the model and the docs still said "available today", but calls failed, because the switch was thrown upstream at the model.
- A new failure mode: regulatory. It fires for everyone at once, with no notice and no date for when it lifts. EUC has muscle memory for outages, deprecations and price changes, not for this.
- Keep the separate 22 June pricing change (Fable 5 moving to usage credits) apart from the government order.
- Practical: know which agents stop if their model goes away, treat the model as swappable, and have a fallback that is wired and tested. Opus 4.8 stayed up and is a capable fallback.
- Options today: the Foundry model router (several models behind one endpoint, automatic failover with at least two models; for Claude still in preview and you deploy the models yourself first) or failover in your own code.
- Limits: failover was built for wobbly endpoints, not for a model pulled by a directive, and a different model behaves differently, so test the fallback.
- The model is an enterprise asset too, next to the agent's identity, scope and logs, and its availability is not fully in your or the vendor's hands.

## Full text (as published)

> The story doing the rounds this week is more of a political one, a new frontier model that showed up in Microsoft Foundry on a Monday and was switched off worldwide by Friday, and while it is a big story on its own, the question I have sits a little closer to our own work.
>
> What we will cover:
> 🔹 The odd in-between state where Foundry still lists the model and still reads "available today", while a call to it quietly fails
> 🔹 A new kind of failure, a regulatory one, that can fire for everyone at once with no notice and no date for when it lifts
> 🔹 What you can do about it today, the Foundry model router and the fallback options, where they help and where they do not quite reach yet
>
> What happens to the agent you built when the model underneath it disappears? And not from an outage or anything you changed but because a letter arrived.
>
> **Quick recap of what happened**
> On the ninth of June, Microsoft made Claude Fable 5, Anthropic's newest and most capable public model, available in Microsoft Foundry, in Foundry Agent Service and in GitHub Copilot.
>
> The same day it also went live on AWS and on Google Cloud, a broad multi-cloud launch aimed at long-running agent work, the kind of multi-step, plan-and-execute tasks a lot of us have been prototyping.
>
> Three days later, on the twelfth, the US government issued an export control directive citing national security, suspending access to Fable 5 as well as Mythos 5 for any foreign national, inside or outside the United States.
>
> And because there is no straightforward way to block only foreign nationals in real time, Anthropic disabled both models for every customer everywhere to stay compliant, while leaving all its other models, Opus 4.8 included, running normally.
>
> Both sides have put their view on the record, and it is worth holding them next to each other rather than picking one.
>
> The government, through the directive and through later comments from David Sacks on the administration's side, frames it around a method of bypassing the model's safeguards, with the route back being that Anthropic closes that bypass.
>
> Anthropic says the jailbreak in question is narrow, that the capabilities it exposes are minor and already obtainable from other public models including OpenAI's GPT-5.5, and that it is complying with the order while disagreeing that a finding like this should pull a model used by hundreds of millions of people.
>
> I am not going to tell you who is right or pick a side here, the facts are still moving and part of it is not public, but you can see the shape of the disagreement.
>
> One thing to keep separate while you read the coverage, there is also a pricing change coming on the twenty-second of June, where Fable 5 moves off the included plans onto usage credits, that is a capacity decision from Anthropic and has nothing to do with the government order, two separate things that are easy to mix up.
>
> Now to the bit that matters if you went and wired this in (you probable didn't though).
>
> At the time of writing, In Foundry the listing is still there, the documentation still names it as an available model, the launch blog still reads available today, and yet a call to it fails, because the switch was thrown upstream at the model itself and not in the catalog.
>
> So, you get this in-between state, a model that still shows up in the picker but will not run, and if you built an agent against it last week that agent is now sitting on an engine that is technically still listed and not running at all.
>
> **They might know something we do not.**
> In EUC we have years of muscle memory for certain kinds of failure, a service has an outage and then it comes back, a version gets deprecated but with a long runway and a migration path to follow, budgets shift when a price changes and you re-plan, all of that we have done before. Heck, we even moved from on-prem to cloud, back to on-prem and now to hybrid. However, we took our time while doing so.
>
> I would argue that it has never moved as fast as we have seen over these last couple of months. The speed at which Ai evolves is very unlike anything we have seen before in the world of EUC.
>
> What we have not had to design until now, is the model under an agent being removed overnight for reasons that have nothing to do with our tenant, our config, our region or even the vendor's own choice.
>
> While the reason is more politically tainted, this could also happen with existing models, for reasons we cannot yet think of.
>
> The model has become a dependency with a failure mode we did not have on the list, a regulatory one, and it can fire for everyone at once, with no notice and no clean date for when it lifts.
>
> **What that means in practice is fairly down to earth, and none of it is dramatic.**
> If you are prototyping agents, and a lot of us are, it is worth knowing which of your agents would stop tomorrow if their model went away, and treating the model as something you can swap rather than something the agent is tied to, a fallback that is already wired and tested instead of one you will build later when you need it.
>
> Opus 4.8 stayed up through all of this and is a capable place to fall back to, and the broader point holds whichever models you use, the agent and the model want to be loosely coupled enough that losing one model is a config change rather than a rebuild.
>
> There are ways to set this up today, though they are more limited than you might hope.
>
> The cleanest one sits in Foundry itself, the model router, where you put several models behind a single endpoint and it falls over to the next one on its own when a model stops responding, as long as you have given it a set of at least two to pick from, and you can point a Foundry agent at that router so the agent inherits the same failover.
>
> With the catch that for the Claude models this routing is still in preview and you have to deploy them yourself first before the router can reach them, so it helps, but it is not (yet) a switch you flip and forget.
>
> You can also do it a layer down in your own code, catching the failure or the refusal and retrying on another model, which is close to what Anthropic itself suggests for Fable.
>
> And either way it is worth being clear about how far this goes, this kind of failover was built for a model that hiccups or has a wobbly endpoint rather than one pulled out from under you by a directive, though to your agent the two look much the same, the endpoint stops answering.
>
> So it only saves you if another model in the set can actually carry the work, and since a different model can behave differently you want that fallback tested rather than assumed.
>
> If your pipeline pins a single model with no path off it, this episode might be a cheap reminder to fix that while the stakes are still a prototype. You're welcome.
>
> The whole pitch of the agent era, the one running through Agent 365 and Windows 365 for Agents and all the identity work, is that an agent is something you can govern like any other enterprise asset, give it an identity, scope what it can do, keep the logs, retire it when you are done.
>
> This past week adds a line to that picture we will have to get used to, the model the agent runs on is an asset too, and its availability is not entirely in your hands, or even in the vendor's.
>
> I will keep an eye on where this one goes and pull the parts worth knowing out as it moves.
>
> Thank you for reading!
>
> BvK.

## Verwante notities

- [EUC News Nuggets on LinkedIn: the newsletter and its editions](euc-news-nuggets-linkedin-newsletter.md)
- [The model under your agent is a dependency that can disappear](positie-model-availability-is-a-dependency.md)
- [Build model-agnostic, the model is part of your supply chain](positie-build-model-agnostic.md)
- [Newsletter: Seven new AI models, and why that is not the point](bron-nieuwsbrief-2026-seven-ai-models.md)
