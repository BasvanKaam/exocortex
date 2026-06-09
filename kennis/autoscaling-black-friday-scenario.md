---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [autoscaling, scale-sets, scaling-plans, load-balancer, scaf]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Autoscaling and the Black Friday Scenario

A scenario Bas has experienced first-hand. Take a company hosting its e-commerce platform in the cloud (e.g. Azure) running a big sale like Black Friday. Normally traffic is stable, but during the sale user numbers spike exponentially.

If the environment isn't set up for autoscaling, or there are limits on resources that can be auto-assigned (CPU, memory, network capacity), the platform struggles, leading to: slow page loads, transaction time-outs, systems crashing from overload, and customers leaving (and staying away). This directly hits revenue and customer satisfaction at a crucial moment.

Mitigations Azure offers: Scale Sets for 'normal' virtual machines, and Scaling Plans for Azure Virtual Desktop hosts, to auto scale VM counts up/down by load and time of day. Third-party solutions can start/stop/build/delete VMs based on actual VM load through the day. Load balancers distribute traffic evenly across systems to keep performance stable at peaks.

Bas notes the book doesn't deep-dive into architecture design (other good books exist), but mapping these issues IS part of his Step-Cloud Adoptie Framework (SCAF), specifically the Inzicht (Insight) and Uitvoering (Execution) chapters. His mantra: a good preparation is half the work — the right knowledge and expertise in the right place.
