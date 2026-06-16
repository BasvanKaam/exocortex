---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [cloud, azure, aws, data-sovereignty, latency, adoption]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Durable barriers to public cloud adoption

Reasons Bas listed in 2016 for why companies might stay on-premises or go hybrid, most of which remain valid concerns:
- Company-sensitive data: where it's stored, encryption, who has access, who owns it, privacy and responsibility -- branch/industry dependent.
- Data locality: not all applications work well when physically separated from their data; this stays important even with RemoteApp/XenApp Express and Windows 10 VDI from the cloud.
- Internet dependency: the connection becomes vital ("all eggs in one basket"); bandwidth, latency and jitter drive user experience, especially when app and data are separated. Dedicated links like Azure ExpressRoute or AWS Direct Connect help but cost extra on top of existing connectivity.
- Physical proximity: response times still depend on how close the customer is to a cloud datacenter.

Framing worth keeping: "considering the cloud just because it will be cheaper doesn't make much sense" -- decide based on the problem you're solving, not the hype.

*Bron: blogpost '13 reasons that MIGHT prevent companies from successfully leveraging public cloud services' (2016-08-23), basvankaam.com.*

## Verwante notities

- [AWS Outposts: native AWS services in your own datacenter](aws-outposts-hybrid-native-services-on-prem.md)
- [AWS is still No. 1 in cloud, Microsoft is catching up fast](aws-still-number-one-microsoft-catching-up.md)
- [Azure building blocks to extend, protect and migrate RDS/WVD](azure-services-for-rds-wvd-extend-migrate.md)
- [Bas's list of reasons companies stay (partly) on-premises](bas-objections-to-full-cloud-migration.md)
- [Moving to the cloud does not automatically save money](cloud-does-not-automatically-save-money.md)
- [Cloud is a potential solution, not a silver bullet](cloud-is-no-silver-bullet.md)
- [The cloud is taking over, but in 2016 it is not yet proven for everybody](cloud-is-not-mature-yet-2016.md)
- [A simple DIY method to compare Cloud datacenter latency](diy-cloud-latency-ping-test-method.md)
- [On-prem is still king; a cloud 'big bang' is coming, slowly](on-prem-king-cloud-bigbang-prediction-2018.md)
