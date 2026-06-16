---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, mcs, pvs, positie, application-layering, containerization]
bron: basvankaam-blog
---

# MCS vs PVS is done to death; pick a lens and stress-test the choice

In his first post as a Citrix CTP (Feb 2016), Bas deliberately refuses to write yet another MCS vs PVS comparison ('there are plenty of good ones out there already'). Instead he adopts a clever framing device: he assumes the reader has already chosen MCS (because it's simple and built in) and writes from that reader's perspective ('these are your thoughts, not mine, PVS might be worth considering as well'), then stress-tests the decision with the questions you should still ask. His broader view: virtualizing 100% of app workload won't happen anytime soon, so base images stay painful, and application layering and containerization can help with most app-related issues, but general adoption 'will take some time'. The tone is consultant-pragmatic rather than evangelist.

*Bron: blogpost 'Citrix Machine Creation Services… What to consider!' (2016-02-09), basvankaam.com.*

## Verwante notities

- [Application virtualisation tops out around 70-80% in practice](app-virtualisation-ceiling-70-80.md)
- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [Stance: container concepts carry over from Docker/Linux to Windows](containers-concepts-durable-over-platform.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [Positie: Personal vDisk is great and underappreciated](positie-pvd-underappreciated.md)
- [PVS vs MCS is a race, and Citrix will pick the survivor](pvs-vs-mcs-citrix-will-decide-the-winner.md)
- [PVS vs MCS image-delivery tradeoffs (XenDesktop 7 era)](pvs-vs-mcs-tradeoffs.md)
