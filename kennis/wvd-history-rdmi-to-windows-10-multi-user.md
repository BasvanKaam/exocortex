---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [wvd, rds, rdmi, history, azure]
layer: reference
gedateerd: ja
bron: salomon-wvd
---

# From RDMI to Windows 10 multi-user: how WVD came to be

Bas's narrative of the WVD origin story, as he told it in session (time-bound to 2018-2019):

- Windows 10 from the cloud was originally not possible due to licensing restrictions, unless a full per-customer environment was built; Microsoft later loosened this and designated multiple partners per country.
- **RDMI** (Remote Desktop Modern Infrastructure) was introduced at Ignite 2017 — the technology behind what became WVD. Heavy speculation followed about the fate of the existing shared-server RDS model.
- Early 2018 (March/April): Server 2019 shipped without the RDSH role / multi-user capability, fuelling speculation; the functionality later returned.
- Ignite, 6 September 2018: "Helping customers shift to a modern desktop" — longer Windows 10 support (now 18 months instead of upgrading every 6), Windows as a Service, ProPlus on Server 2016 (to 2025) and 8.1 (to 2023), no ProPlus support on Server 2019.
- 23 September 2018: Windows 10 as a virtual workplace from Azure announced — Azure-only to start, on-prem possibly later, with a simplified Microsoft 365 license model, free extended support for Windows 7, no more RDS CALs (existing licenses reusable), based on Windows 10 Enterprise/Education.
- Target: persistent first then non-persistent; control plane East US only to start (VMs from other regions allowed); one broker per tenant; agent on VM connecting to the control plane; GA mid-2019.

*Bron: Salomon-IT 'MCS sessie' (WVD).*

## Verwante notities

- [Bet: Windows Virtual Desktop Will Be a Major Force in 2019](bet-wvd-major-impact-2019.md)
- [Christiaan Brinkhoff as 'Mister WVD' and the 2020 WVD framing](christiaan-brinkhoff-mister-wvd.md)
- [Cloud-Native Control Plane Changes the Delivery Economics (WVD as Exemplar)](cloud-native-control-plane-changes-economics.md)
- [RDSH vs VDI vs DaaS vs WVD: Single-User and Multi-User Explained](rdsh-vdi-daas-wvd-explained.md)
- [WVD Explained: Bas's Core Story](wvd-explained-bvk-framing.md)
