---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [wvd, architecture, reverse-connect, azure, broker, gateway]
layer: reference
gedateerd: ja
bron: salomon-wvd
---

# WVD user connection flow and Reverse Connect

The connection flow Bas used to explain WVD (2019 state, his own Dutch wording):

1. The user starts the RD client, which connects to Azure AD. The user logs in and Azure AD returns the authentication token.
2. The RD client presents the token to the Web Access service. The Broker queries the database and determines which resources the user is entitled to.
3. The user selects the desired resource; the RD client connects to the Gateway service.
4. The Broker sets up the connection from the host agent to the Gateway. RDP traffic now runs over connections 3 and 4.

**Reverse Connect (security).** Outbound WebSocket connections from the VMs to the Broker and Gateway, bidirectional communication between the VMs and the RD infrastructure over HTTPS (443), and no inbound ports needed toward the VMs.

**Prerequisites (as of launch):** an Azure subscription with sufficient credits, PowerShell cmdlets, a vNet configured with a domain controller as DNS for the VMs, all resources in the same region, a working Active Directory to join machines (admin rights, Azure AD Connect, ADFS optional for SSO), a domain controller or Azure AD Domain Services, and optionally on-prem networking (ExpressRoute, VPN).

*Bron: Salomon-IT 'Windows Virtual Desktop - Nieuw' (WVD).*

## Verwante notities

- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [Windows Virtual Desktop 2019 launch reference](wvd-2019-launch-reference.md)
- [WVD Explained: Bas's Core Story](wvd-explained-bvk-framing.md)
- [WVD is what used to be RDMI](wvd-is-rdmi-on-prem-history.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
