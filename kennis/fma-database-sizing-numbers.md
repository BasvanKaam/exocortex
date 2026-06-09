---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [sizing, central-site-database, monitoring-database, configuration-logging, mcs]
layer: reference
bron: inside-citrix-fma
---

# FMA database sizing numbers

Indication-only figures from Citrix Consulting Services (real-world values vary), in MB.

Site database max size:
- 1000 users / 50 apps / RDSH: 30; 10,000 / 100 / RDSH: 60; 100,000 / 200 / RDSH: 330
- 1000 users / VDI: 30; 10,000 / VDI: 115; 40,000 / VDI: 390

Monitoring database (1 week / 1 month / 3 months), assuming a 5-day week, one connection and one session per user:
- 1000 RDSH: 20/70/230; 10,000 RDSH: 160/600/1950; 100,000 RDSH: 1500/5900/19000
- 1000 VDI: 15/55/670; 10,000 VDI: 120/440/5500; 40,000 VDI: 464/1700/21500

Monitoring data retention: non-Platinum customers can store data up to 7 days; a Platinum license stores all data up to a year, with 90 days as the default.

Configuration Logging database: relatively small without MCS (around 30-40 MB), but with MCS it can easily grow beyond a few hundred MB depending on machines provisioned.

Citrix released the Database Sizing Tool for XenDesktop 7.x (CTX139508) to estimate sizes over time.
