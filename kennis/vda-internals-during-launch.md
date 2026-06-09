---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, portica, ica-service, cgp, thinwire]
layer: reference
bron: inside-citrix-fma
---

# What happens inside the VDA during launch (PortICA/ICA service)

Assuming Session Reliability is enabled and a desktop-OS VDA launches:

1. The CGP service receives the connection and passes it to tcpip.sys, which forwards it to the ICA stack.
2. The ICA stack notifies the ICA Service (PortICA service, picaSvc), which accepts the connection.
3. The ICA Service locks the workstation because the user must be authenticated.
4. As the user logs on, PortICA tells the display manager to change display mode to remote ICA, forwarded to the ThinWire driver.
5. PortICA hands the 'pre-logon' ticket data (received from the ICA stack) up to the Desktop service and back to the Controller in exchange for real credentials.
6. The Desktop service receives the user's credentials and sends them back to PortICA.
7. PortICA contacts the authentication service to log on the user.
