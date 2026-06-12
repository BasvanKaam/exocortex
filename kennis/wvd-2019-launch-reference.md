---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [wvd, azure, rds, fslogix, reference]
layer: reference
gedateerd: ja
bron: salomon-wvd
---

# Windows Virtual Desktop 2019 launch reference

Reference captured from a Microsoft Cloud Infrastructure Summit deck (18 April 2019), summarising WVD as announced. Time-bound to the 2019 product state.

**Positioning.** WVD is "the best virtual desktop experience, delivered on Azure": optimized for Office 365 ProPlus, the only multi-user Windows 10 experience, integrated with Microsoft 365 management/security, and including Windows 7 extended security updates at no charge. Entitlement is bundled in Microsoft 365 E3/F1, Windows 10 Enterprise E3/E5, Windows 10 VDA per user, and RDS CAL (incl. SPLA).

**Three virtualization hosts of the future:** Windows 10 Enterprise multi-session (modern, multi-session, Win32+UWP, O365 ProPlus, Semi-Annual, Azure-only); Windows Server RD Session Host (legacy, Win32, Office 2019 perpetual, LTSC, on-prem); Windows 10 Enterprise single-session.

**Reverse Connect** improves isolation: outbound WebSocket connections from VMs to Broker/Gateway, bidirectional over HTTPS (443), no inbound ports opened on the VM.

**Shared-responsibility split:** Microsoft manages the Azure control plane (Broker, Gateway, Web Access, Diagnostics); the customer manages the Azure VMs, AD, profile file server, and Azure SQL DB.

**Deployment/management options:** onboarding via Azure Marketplace or GitHub ARM templates; manage via REST APIs, PowerShell (best for repeatable/DSC), or Terraform/partner tooling.

**Migration models:** burst-to-Azure (active-active, dynamic scaling) and disaster recovery (Azure Site Recovery, active-passive). **EOL drivers:** Windows 7, Server 2008/2008 R2, Office 2010, SQL Server 2008 reaching end of support (Jan 14, 2020).

*Bron: Salomon-IT 'iSense Cloud Infra Summit RDS-WVD' (WVD).*

## Verwante notities

- [Bet: Windows Virtual Desktop Will Be a Major Force in 2019](bet-wvd-major-impact-2019.md)
- [Christiaan Brinkhoff as 'Mister WVD' and the 2020 WVD framing](christiaan-brinkhoff-mister-wvd.md)
- [CloudJumper optimization features, platform VM, and pricing (2019)](cloudjumper-optimization-features-and-pricing-2019.md)
- [CloudJumper portfolio: CWMS, CW for Azure, and WVD integration](cloudjumper-portfolio-cwms-cw-for-azure-wvd.md)
- [Microsoft deliberately leaves WVD management gaps to partners](positie-microsoft-leaves-wvd-management-to-partners-on-purpose.md)
- [WVD user connection flow and Reverse Connect](wvd-user-connection-flow-and-reverse-connect.md)
