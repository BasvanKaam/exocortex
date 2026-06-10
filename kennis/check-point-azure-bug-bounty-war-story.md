---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [security, check-point, azure, bug-bounty, war-story, azure-stack]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Check Point and the Azure tenant-isolation bug bounty

Bas tells the story of Check Point Software Technologies, a global cybersecurity firm founded in 1993, based in Israel, known for a broad range of security solutions focused on preventing cyberattacks. Its research teams (Check Point Research) hunt new threats and vulnerabilities, sharing findings with the wider industry and partnering with companies like Microsoft. Bas notes Check Point is a respected leader (especially in network and cloud security) but not the only standard — peers include Palo Alto Networks, Cisco and Fortinet.

The war story: a few years ago, after earlier going after WhatsApp, TikTok and Zoom, Check Point's turn came for Microsoft Azure. Companies like Microsoft, Google and AWS offer 'bug bounties' to researchers for finding vulnerabilities, and Check Point can join such programs at the company's request for a financial reward. The Azure test had far-reaching consequences: the isolation between tenants could be broken, making it possible to intercept, view and even modify code from other tenants. The severity was rated a perfect 10.0 on the security-risk scale.

A key nuance: Check Point ran the tests not on the live Azure cloud but on the offline Azure Stack (HCI), a near-identical replica of Microsoft's cloud environment. After the vulnerabilities were found, Microsoft confirmed they would also be present in the cloud, patched them, and rewarded Check Point with a bug bounty. Bas's takeaway: this underscores the importance of collaboration between security researchers and cloud providers to find and fix threats before malicious actors can exploit them.

## Verwante notities

- [Hyperscaler security investments and certifications](cloud-provider-security-investments.md)
