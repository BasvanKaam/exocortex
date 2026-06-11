---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [iot, azure, big-data, fujitsu, use-case]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# The Connected Cow: an IoT + cloud big-data use case

A durable illustrative use case (Fujitsu, recounted by Bas in 2017). Problem: a cow is only fertile during the Estrus phase, recurring on average every 21 days, with a mating window of roughly 12 to 18 hours (highest success 10PM to 8AM). On farms with thousands of cows, manually catching that window is impractical, and historically artificial insemination (AI) was only about 50% accurate on timing, yielding around a 35% pregnancy rate.

Solution: cows show markedly increased movement (more steps/small jumps) as Estrus approaches. Fujitsu-built pedometers (5+ year battery, antenna with ~300m range) relay step data via a 3/4G router to a base station and on to the Azure cloud, where big-data analysis flags abnormal movement and alerts the farmer. Detecting the mating cycle this way succeeded in ~95% of cases, lifting pregnancy success from ~35% to 65+% and cattle production up to 70%. The same movement data could proactively detect 8 to 10 diseases. A further finding: AI in the first half of a ~16-hour window after movement change yields female calves ~70% of the time, the second half yields males ~70% of the time.

Why it matters as a pattern: cheap distributed sensors plus cloud analytics turning raw behavioural data into precise, actionable decisions, which Bas calls a true added advantage of cloud computing.

*Bron: blogpost 'IoT use-case: The Connected Cow! Yes, really.' (2017-04-04), basvankaam.com.*

## Verwante notities

- [Citrix Octoblu: an everything-is-a-node IoT platform](citrix-octoblu-architecture.md)
- [Take: big-data analytics is the real advantage of the cloud](cloud-analytics-real-advantage-stance.md)
- [Industrial IoT will be the biggest sub-vertical (2017 call)](iiot-the-next-big-thing-2017.md)
- [IoT is a mindset shift; answer the business questions before the tech](iot-strategy-before-technology.md)
- [The three-block IoT architecture: Edge, Platform, Enterprise](iot-three-block-architecture.md)
