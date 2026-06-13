---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmw, licensing, avd, wvd, cost, dated]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Named vs concurrent user licensing, and the 30-day peak rule

Durable AVD/Nerdio licensing concept, captured from an early NMW KB (specific dollar rates omitted as pricing). The mechanics generalize beyond any one product version.

**Two models:**
- **Per-named user** - billed on the maximum number of unique users *assigned* to host pools at any point in the past 30 days.
- **Per-concurrent user** - billed on the maximum number of unique users *connected* to host pools at any point in the past 30 days. Per-concurrent carries a higher unit rate than per-named.

**The rule that drives the bill:** every month the system inventories the rolling 30-day peak for whichever metric your license type uses (assigned vs connected). That peak count is what gets billed (through Azure, on the 1st of the month).

**De-duplication:** a single user assigned to (or connecting from) multiple host pools is counted once, not per pool.

**The choice:** named is cheaper when many users are entitled but rarely all online at once is not the case; concurrent is cheaper when you have a large entitled population but only a fraction connect simultaneously. Pick the model that produces the lower bill for your actual usage shape; for named you only care about peak *assigned*, for concurrent only peak *connected* - the other number is irrelevant to your cost.

*Bron: Nerdio-content 'KB - Nerdio Manager for WVD license count and invoicing' (KB Articles).*

## Verwante notities

- [NMW architecture: PaaS-only deploy, metering-only billing](nmw-paas-architecture-and-billing-model.md)
