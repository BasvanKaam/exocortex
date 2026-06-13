---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloud, hybrid, saas, iaas, governance, essay]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# The cloud's promises, line by line (Bas's reality check)

From Bas's 2019 essay. He grades each commonly marketed cloud promise against reality. Durable as a framework for cutting through cloud marketing; some specifics (capacity, regions) are 2019-dated.

NIST core characteristics (still the baseline): on-demand self-service, broad network access, resource pooling, rapid elasticity, measured service.

The promises, graded:
- **Cheaper** -> not necessarily. Pay-per-use often costs more over long periods. 1/3/5-year commitments unlock discounts. Don't forget one-off transition/migration costs. Cloud is framed as Opex but there's more to it; many realize this too late. Real value is elsewhere: shorter time-to-market, immediate availability, less operational overhead, scalability, temporary use, flexibility, which often drive savings in other areas.
- **More secure** -> agreed. Very few organizations can spend hundreds of millions annually on security; the provider can.
- **Instantly available** -> true, but depends on service and scale (spinning up a thousand VMs still takes time; warn your provider rep at that scale).
- **Easy to use** -> not entirely. Holds for SaaS (form + credit card). With IaaS you still own OS, apps, data, AV, encryption, auth; only hardware and hypervisor are abstracted.
- **Infinite scalability** -> partially. Physical datacenter limits are showing (power constraints, capacity caps in some regions).
- **Available everywhere** -> true, given a working internet connection.
- **Always available** -> no. Outages remain relatively common and always cost productivity.
- **Open standards** -> only to some extent. APIs are the closest thing; vendor lock-in is real; portability is weak, which is why a cloud exit strategy matters.
- **Hands-off management** -> depends on service, and even then not guaranteed; with a modern digital workspace, DaaS, PaaS and especially IaaS you still keep OS/apps/data secure and current.
- **Innovative** -> absolutely.

Core principle: 'Use cloud services where they make sense and where they add real value. If there's no added value, there's no reason to move.'

*Link to: position-cloud-first-not-cloud-only.md, cloud governance notes.*

*Bron: Nerdio-content 'Cloud only No. Cloud First or Hybrid Yes.' (Blogs).*

## Verwante notities

- [What actually slows cloud adoption (and why cloud-first beats cloud-only)](cloud-blockers-and-the-cloud-first-case.md)
- [Physical and performance limits of working from the cloud](cloud-physical-and-performance-limits.md)
- [Cloud-only is a utopia; cloud-first or hybrid is the only honest answer](positie-cloud-only-is-a-utopia.md)
- [Have a cloud exit strategy; lock-in and weak portability are real](position-cloud-exit-strategy.md)
- [Cloud only? No. Cloud first or hybrid? Yes.](position-cloud-first-not-cloud-only.md)
- [The promises of the Cloud (and Bas's invitation to challenge them)](the-promises-of-the-cloud.md)
- [Why traditional Windows apps keep hybrid alive for decades](why-windows-apps-keep-hybrid-alive.md)
