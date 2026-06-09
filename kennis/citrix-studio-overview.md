---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-studio, management-console, broker-service, delivery-controller, powershell]
layer: reference
bron: inside-citrix-fma
---

# Citrix Studio: the central management console

Citrix Studio is THE management console for administering, configuring and managing XenDesktop and/or XenApp Sites from a single pane of glass. It provides access to real-time data collected through the Broker service running on the Delivery Controller. FMA fact: by default Studio communicates with the Controller on TCP port 80.

Typical setup order: create the primary Site, then a Machine Catalog, then a Delivery Group, then publish applications/desktops. From Studio you control the entire Site (Zones, Machine Catalogs, Delivery Groups, Delivery Controllers, VDAs, etc.), integrate StoreFront and App-V, add and configure Host Connections, manage MCS, set up delegated administration, and configure policies.

FMA fact: Studio doesn't cover everything. Provisioning Services has a separate management console, as does Citrix NetScaler.

Studio offers basic troubleshooting: self-diagnostics tests on Delivery Groups, Machine Catalogs and Site-wide; launching PowerShell directly (and auto-generating PowerShell scripts for almost anything Studio does); policy tools (overview of all settings, filters, policy comparison, Group Policy Modelling, Citrix Group Policy Modelling). Resultant Set of Policies (RSOP) is only available via the GPMC approach. Studio also shows license usage, lets you restart/shutdown machines, message and log off users, and place machines/Catalogs into maintenance mode.
