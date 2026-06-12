---
type: positie
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloud-migratie, principes, cloud-native, cloud-exit, disaster-recovery, regie-organisatie]
bron: salomon-opdrachten
---

# Positions I apply in a cloud transition

Reusable principles I bring to cloud migration engagements, independent of the specific client.

## Cloud-native over IaaS
Prefer cloud-native (PaaS) over lifting-and-shifting into IaaS VMs. Every database or service you can run as a managed PaaS offering is "one less IaaS VM" to own and maintain. The hyperscaler choice often follows existing investment: heavy existing use of a productivity suite makes that vendor's cloud the most logical landing zone.

## Start small and test
Begin with a low-risk first workload and explicitly plan for application testing. A jump across several OS generations (e.g. server 2008/2012 to 2016/2019, or Windows 7/8 to 10) is bigger than people assume. Pick a first workload with no complex dependencies, well documented, easy to test, no access to protected data, and ideally splittable into smaller steps. Vendor compatibility programs can help where app compatibility is the blocker.

## Question the full desktop
A published full desktop is often up for discussion, rightly so. Once a modern collaboration way of working (chat + document collaboration) is in place, a full desktop becomes redundant. Managed laptops plus a relatively simple remote-app environment for the remaining applications usually fits better and can be delivered securely and location-independently.

## Disaster recovery is a standard attention point
DR is in my approach by default. When the bulk of infrastructure lives in the cloud, arranging DR becomes much simpler, and that benefit extends to the systems that stay on-premises too. Backup cadence (daily/weekly/monthly/yearly) and an offsite backup are baseline expectations.

## Cloud exit strategy as insurance
Not a popular topic, but important. I recommend thinking through a cloud exit strategy. See it as insurance: wonderful if you never need it, but you're glad it exists and that you gave it attention in time.

## The move to a regie (orchestration) organization
When an IT department shifts to consuming services and becomes an orchestration/vendor-management function, assess the organizational impact early. With a small, capable team this transformation usually has limited day-to-day impact, but it deserves explicit attention rather than being assumed away.

## Knowledge gaps are closable, name them anyway
A small knowledge gap is normal and usually closes with a few trainings plus hands-on work; the learning curve is rarely steep. Still, make risks and knowledge gaps explicit in the Insight phase rather than waving them off. I can advise on the training path or fill it via my own Academy.

## Adoption is not optional
End-user impact and org-wide adoption of a new way of working are easy to skip and shouldn't be. Timely communication about what's coming, a focus on the benefits, and clear routes to information/training/instructions raise the odds of success and lower the load on the internal IT team.

## Related
- See `cloud-adoptie-framework-vier-pijlers.md` and `cloud-inventarisatie-methode-waves-en-rs.md` for where these positions apply in the engagement.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (research and development organization (private research institute)).*

## Verwante notities

- [Bas on disaster recovery: no blueprint, and don't forget the BUDGET](bas-on-disaster-recovery-and-budget.md)
- [Cloud adoption framework: four phased pillars](cloud-adoptie-framework-vier-pijlers.md)
- [A cloud exit strategy is insurance you hope not to need](cloud-exit-strategy-as-insurance.md)
- [Compare cloud to cloud, not cloud to on-prem](cloud-fit-compare-cloud-to-cloud.md)
- [Cloud inventory method: joint assessment, waves, and the R's](cloud-inventarisatie-methode-waves-en-rs.md)
- [Criteria for Selecting the First Workload to Migrate](first-workload-selection-criteria.md)
- [Position: phase the rollout and keep part of the legacy estate intact](position-phased-rollout-keep-legacy-intact.md)
- [Principles I apply on transformation engagements](transformation-principles-positions.md)
- [The Two-Scenario Offer: Centralized Backend vs Managed-Laptop-Only](two-scenario-offer-pattern.md)
- [Proposal structure: conversation recap plus first impression under reservation](voorstel-structuur-eerste-indruk.md)
