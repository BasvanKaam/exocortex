---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, licensing, grace-period, high-availability]
layer: reference
bron: inside-citrix-fma
---

# Citrix license grace periods and supplemental grace period

If the License Server cannot be contacted, users and products are protected by a **grace period** with no interruption or loss of functionality. XenDesktop stores a local replica of the licensing information (number and type of licenses), and when the connection is lost it enters the grace period using that cached data. The maximum grace period is usually **30 days** (may differ slightly per product). Infrastructure components and the license server exchange heartbeat messages every **five minutes**; when the heartbeat fails the grace period kicks in. Event Viewer messages show that a product has entered a grace period and the time remaining.

As of version 7.6 Citrix added a **supplemental grace period**: when all licenses are in use it lets users keep connecting for a default of **15 days** with no connection limit, after which normal limits are enforced and new connections are refused. It is granted per product, per edition and per Subscription Advantage Eligibility date, and only for Retail licenses. This replaced the old model of granting roughly 10% overdrafts above the license count.

Making the license server highly available is optional (the grace period covers outages by default), but if you already run a NetScaler you can load balance two license servers in an active/passive setup.
