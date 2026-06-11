---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [performance, latency, printing, office-365, limitations]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Physical and software performance limits of the cloud

In his paper Bas details performance constraints. The internet connection becomes a crucial component: lack of bandwidth, latency or outages hurt the user experience. A Direct Connect / ExpressRoute helps but is far too costly for most organisations, redundant connections are a must, and it doesn't solve the remote-worker problem. Physical distance and multiple hops add up. You're also bound to the services and prices offered per region, which differ across regions for every large provider.

His claim: it is virtually impossible to match on-premises performance in a cloud environment with the same configurations (network, memory, CPU, storage) — cloud carries a certain overhead. Machines must almost always be sized heavier just to approach local speeds, and even then it's hard.

Two concrete examples:
- **Printing** — fast printing remains a challenge, especially using existing on-prem print infrastructure; uncompressed raw print traffic crossing the internet or a limited site-to-site link adds delay.
- **Non-persistent systems / Office 365** — local and user-profile data aren't kept and must be reloaded each login. For Exchange the online mode doesn't work well; most fall back to cached mode, copying the last 3-6 months of mail into the profile (.OST file). The profile grows, so loading takes longer. Solutions exist, but each adds another layer to the stack — making it more complex and laborious. "That can't be the intention of cloud, right?"

## Bron-citaten (NL, verbatim)

> Dat kan niet de bedoeling van Cloud zijn, toch?

## Verwante notities

- [Autoscaling and the Black Friday Scenario](autoscaling-black-friday-scenario.md)
- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Bas's list of reasons companies stay (partly) on-premises](bas-objections-to-full-cloud-migration.md)
- [Prediction: more cloud outages as datacenters hit capacity](cloud-outages-and-capacity-prediction.md)
- [Hybrid cloud: best of both worlds via ExpressRoute and low latency](hybrid-cloud-best-of-both-worlds.md)
- [Hybrid Latency and the Region-Choice Pitfall](hybrid-latency-region-choice-pitfall.md)
- [Bas on cloud, hybrid and the future of on-premises VDI](is-cloud-vdi-still-relevant-takeaways.md)
- [Bas's warning: Cloud apps with on-premises backends invite latency trouble](latency-cloud-app-onprem-backend.md)
- [Performance and Stability: You Trade Control for Provider Scale](performance-stability-and-provider-scale.md)
- [Comparing a Physical Server to Cloud Isn't Fair](physical-vs-cloud-server-not-fair-comparison.md)
