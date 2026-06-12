---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [high-availability, design, opinion, consulting]
bron: basvankaam-blog
---

# On over-engineering HA: simplicity often wins, but it all depends

In the December 2013 comment thread on this post, Bas lands on a balanced consultant's position about SQL HA design. He agrees with a commenter's "don't over-design with fancy features that add complexity while there's an acceptable solution," while pushing back that exploring options never hurts and that "in some cases, simplicity just doesn't cut it" (his recurring "think big" refrain).

He even concedes that doing nothing, paired with a solid monitoring solution and accepting manual intervention, can be a legitimate choice depending on the availability demands and business case. His honest framing throughout: "Like many consultants will tell you... It all depends." He is also candid about the limits of his own knowledge here: "an overview without too much technical details, I simply don't know the products well enough."

*Bron: blogpost 'XenDesktop SQL High Availability... What to use?!' (2013-12-16), basvankaam.com.*

## Verwante notities

- [Fault-Tolerance Decision Hierarchy (Application HA Before Hypervisor HA)](fault-tolerance-decision-hierarchy.md)
- [Why the FMA Site database is a single point of failure (no Local Host Cache)](fma-no-local-host-cache-db-dependency.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
- [VIAB isn't for everyone, but with the right business case it just feels right (May 2013)](viab-given-the-right-business-case-it-feels-right.md)
- [VIAB vs XenDesktop: simplicity vs flexibility tradeoffs (2013)](viab-vs-xendesktop-tradeoffs.md)
- [HA options for the XD7 Site configuration database](xd7-site-db-ha-options.md)
- [XenDesktop 7.6 HA options before Zones](xendesktop-76-ha-options-pre-zones.md)
- [SQL HA options for the XenDesktop Site database and when each fits](xendesktop-sql-ha-options.md)
