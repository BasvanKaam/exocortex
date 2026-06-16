---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [windows-365, avd, cost-control, shared-mode, gpu]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Windows 365 Cloud PC - Pros, Cons and Cost Control vs AVD

**Advantages:** simple deployment and cost predictability — instead of variable usage-based costs (as with AVD), W365 offers a fixed monthly price per user, easing budgeting and avoiding surprises from usage fluctuations. Cloud PCs are **always on** (Frontline is the exception) and **persistent** — Bas notes at time of writing a non-persistent variant called **'Shared Mode'** is in public preview, resetting the Cloud PC on logout. Always-on availability is attractive for home workers and external teams. W365 generally requires less technical expertise; Microsoft takes much infrastructure management (hardware maintenance, network settings, back-end config) off your hands.

**Disadvantages:** the fixed price structure can be more expensive long-term for organisations with heavy fluctuations in user count or resources. W365 offers far less (virtually no) flexibility than AVD for configuring/optimising desktops — e.g. you cannot autoscale (auto on/off, or build/delete machines on the fly). In other words, it's not Pay-as-you-go. It's primarily designed for single-user environments, so each user needs their own VM, which can raise costs at scale. For multi-user scenarios like call centers or generic desktop needs, AVD is usually more efficient.

**What Microsoft handles vs you:** Microsoft fully manages underlying physical systems, storage, networks and core components (no worrying about hardware faults, power — "althans dat is de belofte"/at least that's the promise). You still manage the desktop experience via Intune (depending on variant): installing apps, configuring security, monthly patching, managing user rights. Data security, access management and compliance largely stay with the organisation (see Chapter 10).

**Cost control vs AVD:** AVD gives more cost control via flexibility and scalability — dynamically scale on usage (extra capacity at peak, switch off unused resources off-hours), a true pay-as-you-go model good for variable workloads or temporary projects. AVD can optimise specific VM configs, e.g. assigning GPU capacity (some Cloud PC variants support GPUs too) for graphics-intensive workloads combined with multi-user sessions to lower per-user cost — potentially significant long-term savings if well managed.

Bas's caveat: all of this applies at time of writing (early 2025); given Microsoft's strategy on this topic he expects many changes and announcements in the coming year(s).

## Bron-citaten (NL, verbatim)

> Met andere woorden, het is geen Pay as you Go.
>
> Vergeet niet, dit alles is van toepassing ten tijde van schrijven (begin 2025)

## Verwante notities

- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [Bas's reframe: is AVD and/or Windows 365 Cloud PC really DaaS?](is-avd-and-windows-365-really-daas.md)
- [Simplicity comes at the cost of flexibility](simplicity-costs-flexibility.md)
