---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, registration, health-assistant, troubleshooting]
layer: reference
bron: inside-citrix-fma
---

# Troubleshooting the VDA registration process and Citrix Health Assistant

Within the FMA, VDAs must register with a Delivery Controller or they are of little use. Citrix provides guidance for troubleshooting registration (CTX136668).

The Citrix Health Assistant (version one) focuses on VDA registration issues for both XenDesktop and XenApp, running automated health checks to identify common root causes. It is GUI-based but supports command line. Checks included:
1. VDA machine domain membership verification
2. VDA software installation and relevant services status
3. VDA communication ports status
4. VDA services status
5. Windows firewall configuration
6. VDA communication with Delivery Controllers (DDC)
7. VDA time sync with each DDC

Reference and download: CTX207624.
