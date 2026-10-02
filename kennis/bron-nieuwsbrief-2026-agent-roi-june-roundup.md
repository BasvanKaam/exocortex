---
type: bron
merk: bvk
domein: ai-tooling
status: actief
datum: 2026-10-02
tags: [linkedin, nieuwsbrief, eucnewsnuggets, agents, roi, foundry, roundup, build-2026]
bron: linkedin-nieuwsbrief
---

# Newsletter: Agent ROI in Foundry + June 2026 roundup (no. 10)

Edition no. 10, early July 2026, "my last newsletter before I leave on PTO for a couple of weeks." Two parts: an opinion piece on Microsoft's private-preview agent ROI measurement in Azure AI Foundry, and the monthly June 2026 roundup across AVD/Windows 365, Azure, Intune, AI and Nerdio. The roundup is external news curation and is not distilled into kennis; the opinion part is.

## Part 1: Agent ROI (core points)
- Foundry private preview measures agents by business outcome, not only run cost: task completion, time saved, cost efficiency; compare versions, daily trend, open the traces behind a poor result. Microsoft calls it ROI for agents.
- You pick the value measure (built-in such as task completion, case deflection, customer satisfaction, or your own) and set what a passing result is worth. Rolls up to net value, total cost and current ROI. Framework-agnostic.
- Leadership keeps asking "we paid for this, what are we getting back", and rightfully so. Agents are "like the Oprah show, everyone gets one."
- The catch: you set what a pass is worth, so a soft definition hands you a flattering number. Read any early ROI screenshot with that in mind, your own included.
- Private preview, no GA date, and joining requires bringing your own definition of value.
- What he would do: do not wait for GA. Pick one agent, write down this week what a good outcome is worth in real numbers, before you touch a dashboard. "Start with the end in mind."
- Not Microsoft-only: it runs on traces, so LangChain, OpenAI SDK or Microsoft's framework, GPT or Claude, can be lined up the same way. The pull is Application Insights underneath, which he is personally fine with.
- Side note: Copilot in Microsoft Forms rebuilt around the M365 Copilot chat pane; core landed around March 2026; branching still basic.

## Part 1: full text (as published)

> This one sits a bit under the radar, so I thought it would make sense to highlight it a bit more. My last newsletter, and number 10, before I leave on PTO for a couple of weeks.
>
> Microsoft is testing a way, still private preview in Azure AI Foundry, to measure an AI agent by its business outcomes and not only by what it costs to run (meaning, all the AI token fluff and slop that has been going around lately).
>
> We'll focus on the above, but I have included some other info that you might like as well, all related, of course. Just in case you are already a bit further, which might include other platforms and agent types as well.
>
> **Back on topic…**
> Task completion rate, time saved, cost efficiency, and so on, shown in the Foundry portal or through the API. You can compare versions of an agent, see the trend per day, and open the traces behind a poor result.
>
> Microsoft even calls it exactly that, ROI for agents.
>
> You pick the measure that decides what "value" means here, either one of the built-in ones like task completion, case deflection or customer satisfaction, or your own, and then you set what a passing result is actually worth.
>
> It rolls that up into net value, total cost and current ROI in a single view, on top of the tracing Foundry already does, and it works on any framework, so not only Microsoft's own agents.
>
> Almost every AI agent (never mind the platform or model) and Copilot project I see gets the same question from leadership, we paid for this, what are we getting back, and rightfully so. Eventually, it needs to start producing "something".
>
> I mean, it's cool and all that folks who didn't write before now post a blogpost weekly, or multiple times per week even, or that we see visuals we couldn't even dream of not even that many months ago, but real value-adds are still a rare find. Depending on where you work, that is :)
>
> The same applies to agents. It's like the Oprah show, everyone gets one, it seems. But how successful are they really?
>
> That can be tricky to quantify in lot of cases. Now there is a start.
>
> **There is a catch though.**
> Built-in measure or your own, you still set what a passing result is worth, so a soft definition hands you a flattering number.
>
> This approach does force you to finally answer the outcome question, which is good, but it also lets you answer it in your own favor. So be careful.
>
> Take any early ROI screenshot, your own included, with that in mind.
>
> Two other things to keep in mind, for now at least.
>
> It is in private preview, and currently there is no GA date available. And to even join the preview you have to bring your own definition of value first, which is exactly where the effort goes.
>
> Also, Microsoft rebuilt the Copilot part of Microsoft Forms around the M365 Copilot chat pane. From inside the form it can rework your questions, change settings, add branching, and summaries responses.
>
> It can do so worldwide on commercial Copilot licenses. Worth knowing this one is not brand new, the core landed back around March 2026 and Microsoft just keeps building on it. And the branching is still pretty basic, so give it a once-over before you send anything out.
>
> If you are already measuring agent ROI in real environments, I am curious how you define the outcome and what some of the results are that you have seen.
>
> **What would I do with this?**
> First, do not wait for GA.
>
> Pick one agent you already run, and this week write down what a good outcome from it is actually worth to the business, in real numbers, before you touch any dashboard.
>
> That's the low hanging fruit I'd say and maybe even a small first win, if we can call it that.
>
> The teams that pull ahead are the ones who can say, on paper, what they paid and what they got back.
>
> Make sure to define value honestly, measure it against the cost, and you walk into the next leadership meeting with an answer instead of "just" a feeling.
>
> Start with the end in mind, as always (something I've learned from a smart man, I hope he is reading along).
>
> **One last thing…**
> And btw... this is not a Microsoft-only story (though, it might turn into an Azure one, and that's OK).
>
> It runs on the traces, not on which vendor built the agent, so it does not care whether you used LangChain, the OpenAI SDK or Microsoft's own framework, or whether the model underneath is GPT, Claude or something else.
>
> Claude went generally available in Foundry at the end of June, GPT has been there all along. So you can line a GPT agent, a Claude agent and a home-grown one up in the same way.
>
> The catch is the plumbing, your agents have to send their traces and token cost into Application Insights, so there is still an Azure pull underneath.
>
> If that's a "bad" thing I cannot decide for you (but I don't expect it to be). Personally, I am more than OK with that.
>
> Thank you for reading.
>
> BvK.

## Part 2: June 2026 roundup (structure and headlines)
Framing: June was dominated by two themes. Agents (Build 2026 on 2 June repositioned Windows 365 and much of Azure around AI agents, and moved flagship AI products to consumption billing), and a set of quiet breakers (Secure Boot 2011 certs expiring, Autopatch hotpatch on by default, Entra blocking a hybrid-identity attack path, message-center changes). "Read them all or simply pick your category." Each item: link, status/date, what, and "Why it matters."

1. **AVD & Windows 365:** Windows 365 at Build "made for developers and agents" (Dev Box into maintenance mode); Windows 365 for Agents GA (2 June); 32 vCPU size, GPU Select plan, GPU for Flex shared; ready-to-code Windows 11 developer image (preview); context-based redirections for AVD and Windows 365 (preview); RDP Multipath with redundant TCP GA; Windows App 1.2.7214; Siemens NX 2506 multi-user on AVD with NVIDIA RTX PRO 6000.
2. **Azure:** Cobalt 200 VMs (preview); Azure HorizonDB (preview); Microsoft Discovery GA; Azure Files share-centric management GA; Functions Flex Consumption rolling updates GA; Container Apps Confidential Compute GA plus Sandboxes; Claude GA in Microsoft Foundry (29 June); Entra ID for Blob SFTP GA; plus Defender for AWS RDS, DP-100 and AI-102 retired, AI-103 released.
3. **Intune:** releases 2605 and 2606. EAM auto-updates GA; Win32 content requires HTTPS (Connected Cache trap); Multi Admin Approval on Graph calls (HTTP 403); STIG audit baseline; detect and block local AI agents (preview); Vulnerability Remediation Agent on Entra agentic identity (90-day clock); ETG for Apple ADE GA; Android BYOD via AMAPI; EPM and EAM into M365 E5 from 1 July 2026.
4. **AI:** Copilot Cowork GA (16 June, billing from 1 July via Copilot Credits); Copilot Studio new agent experience and multi-model GA; M365 Copilot grounding in Power BI and Dataverse; GitHub Copilot usage-based billing (1 June); Claude Sonnet 5 (30 June); GPT-5.6 preview; Gemini 3.5 Flash computer use.
5. **Under the radar:** Secure Boot 2011 certs expiring; Autopatch hotpatch by default; Entra anti-SyncJacking hard-match block (1 June); Conditional Access enforcement change (15 June) and "require approved client app" read-only (30 June); SharePoint OTP to Entra B2B (MC1243549); Intune Data Warehouse re-platform (MC1188216); EWS block for Kiosk/F1/F3 moved to 1 October (MC1191578); free Windows 10 consumer ESU extended to October 2027; June Patch Tuesday with 200+ CVEs; Teams Live Events retired.
6. **Nerdio:** NME 8.0 GA (v8.0.1, 16 June) with AVD Hybrid on Nutanix AHV (preview), Global Pools and NME-Terraform; NME 8.0 is the last version supporting AVD Classic; 8.0.1 extras (configurable Windows 365 migration batches, Console Connect UK region, ControlUp integration end of maintenance, Advisor per-country Windows 365 pricing).

Closes with "What to action" (six items: Secure Boot certs, MAA-on-Graph and the 90-day agent identity, HTTPS on Connected Cache, Conditional Access audit, Intune Data Warehouse backup, B2B external sharing comms) and "Standing deadlines" (1 July pricing and E5 bundling, 14 July SQL Server 2016 end of support, September AVD classic, 1 October EWS for Kiosk/F1/F3). Sign-off: "Thanks for reading. BvK."

## Reconcile
- The free Windows 10 consumer ESU extension to October 2027 here supersedes the 13 October 2026 end date in the June known issues edition.

## Verwante notities

- [EUC News Nuggets on LinkedIn: the newsletter and its editions](euc-news-nuggets-linkedin-newsletter.md)
- [Define what an agent outcome is worth before you open a dashboard](positie-define-agent-value-before-the-dashboard.md)
- [Newsletter: June known issues edition](bron-nieuwsbrief-2026-06-known-issues.md)
- [Newsletter: 12 (cloud) services about to expire](bron-nieuwsbrief-2026-12-services-expiring.md)
