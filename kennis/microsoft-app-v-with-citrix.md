---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [app-v, management-server, publishing-server, rds-cal, shared-content-store]
layer: reference
bron: inside-citrix-fma
---

# Microsoft App-V components and licensing with Citrix

App-V (with XenDesktop/XenApp) consists of:

- **Management server**: centralised console to manage the App-V infrastructure and deliver virtual apps to the App-V Desktop Client and RDS Client. It authenticates, requests and provides security, metering, monitoring and data gathering, using Active Directory to manage users and applications.
- **Publishing server**: provides App-V clients with apps for specific users and hosts the virtual application package for streaming, fetching packages from the management server.
- **Client**: retrieves virtual apps, publishes them, and manages virtual environments at runtime on Windows devices. Installed on the VDA; stores user-specific settings (registry/file changes) in each user's profile.
- **Licensing**: with Citrix XenApp, Microsoft RDS CALs are needed, and App-V is covered as part of RDS licenses (this does not apply to VDI environments). This changed when Microsoft switched from Terminal Services to Remote Desktop Services; with TS CALs App-V still needed separate licensing.

By adding the App-V Management and Publishing servers into Citrix Studio you can publish App-V apps to users' desktops, streamed over the network. Apps can be pre-cached or pre-published, and a shared content store lets you stream from a central source without copying the package locally. Published App-V apps can launch from the Start menu, via Citrix Receiver, the locally installed App-V client, or the StoreFront web interface. The Citrix Connector for System Center Configuration Manager is also an option (compatible with XenDesktop/XenApp 7.1, 7.5, and announced for 7.7 and 7.8).
