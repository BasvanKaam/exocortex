---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [windows-365, cloud-pc, intune, single-user, avd, daas]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Windows 365 Cloud PC

Windows 365 Cloud PC (W365) and Azure Virtual Desktop (AVD) are both Microsoft-built solutions for delivering virtual desktops via the cloud. They share underlying technologies and similar benefits (centralised data, scalability, remote access) but differ significantly in architecture, management, cost structure and use cases.

W365 Cloud PC offers a virtual desktop that functions like a traditional PC on a desk (and is managed that way too), fully hosted in the cloud. Each Cloud PC is a **dedicated, single-user VM permanently assigned to one specific user**. Management is largely simplified and done via **Microsoft Intune (Endpoint Manager)**, so organisations/providers already using Endpoint Manager can reuse existing processes and knowledge; updates, security patches and configs roll out centrally without deep cloud-architecture knowledge (though Bas notes Intune itself isn't necessarily simple). Unlike AVD — where IT teams dive deep into networking, storage and auto-scaling — Microsoft takes much of this work over for W365.

**Windows 365 Frontline:** a variant for organisations with shift work or part-time staff. One Cloud PC license can be shared by up to three users (and three Cloud PCs), but only one user can be active at a time. Bas stresses this is NOT multi-user — that variant does not exist in the W365 Cloud PC world. Data is kept per user. Cost-efficient for shift-based staff. For true multi-user (multiple users simultaneously on the same VM/apps), AVD remains the designated solution.

Bas: there's no 'silver bullet' — in practice both are often combined, with valid use cases for each. Companies with smaller IT teams more often use Windows 365 Cloud PC. Importantly, W365 Cloud PC comes much closer to a DaaS service than AVD does, whereas AVD could form a component of a DaaS offering.
