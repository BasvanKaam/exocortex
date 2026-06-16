---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloud, performance, latency, office-365, euc, networking]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Physical and performance limits of working from the cloud

Bas's catalogue of physical/software limits that constrain cloud-only working (2019 essay; principles durable):

- The internet connection becomes a critical architectural component. Bandwidth shortfalls, latency, and outages hurt UX. Direct Connect / ExpressRoute help but are too expensive for most; redundant links are a must yet still don't fix the remote-worker case. Physical distance and number of hops matter. Service portfolios and pricing differ by region across all major providers.
- You can rarely match on-prem performance with comparable cloud configs (network/memory/CPU/storage); cloud adds overhead, so you typically over-provision more powerful machines just to approach local performance.
- Printing: fast reliable printing stays hard when on-prem print infrastructure remains; raw uncompressed print jobs traversing the internet or a limited site-to-site link introduce delays.
- Non-persistent systems + Office 365: local and profile data isn't retained, so it re-downloads each login. Exchange 'online mode' (directly in Azure) usually performs poorly; most fall back to 'cached mode', syncing the last ~3-6 months locally into an .OST inside the profile, which bloats profile size and lengthens load/login times. Fixing it means adding yet another layer to the stack: more complexity, harder to manage.

*Link to: why-windows-apps-keep-hybrid-alive.md, FSLogix/profile notes.*

*Bron: Nerdio-content 'Cloud only No. Cloud First or Hybrid Yes.' (Blogs).*

## Verwante notities

- [The cloud's promises, line by line (Bas's reality check)](cloud-promises-reality-check.md)
- [A simple DIY method to compare Cloud datacenter latency](diy-cloud-latency-ping-test-method.md)
- [Hybrid Latency and the Region-Choice Pitfall](hybrid-latency-region-choice-pitfall.md)
- [Bas's warning: Cloud apps with on-premises backends invite latency trouble](latency-cloud-app-onprem-backend.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Cloud only? No. Cloud first or hybrid? Yes.](position-cloud-first-not-cloud-only.md)
- [Why traditional Windows apps keep hybrid alive for decades](why-windows-apps-keep-hybrid-alive.md)
