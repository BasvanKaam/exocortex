---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [msix-app-attach, msix, nerdio, avd, remoteapp, howto]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Setting up MSIX App Attach v2 in Nerdio and publishing apps

My working sequence to get App Attach v2 apps published in Nerdio:

1. Upload the app to Nerdio.
2. Create the App Attach v2 image (it should get an icon next to it).
3. Upload the certificate.
4. Create and deploy a RemoteApp host pool. In HostPool > Properties > AVD Deployment, check **Install App Attach certificates**.
5. Assign your users to the host pool.
6. Applications > App Attach > (app properties dropdown) > HostPool: add your host pool, add your users.
7. HostPool > Applications > RemoteApps > Add Remote App. App Source = App Attach Package; select your app and options.
   - Description, Icon Path and Icon Index aren't required; it defaults to Icon Index 0. If that's the wrong icon, set 1/2/3 etc – icons are indexed inside the app.
8. Give it 30-45 minutes; the first publish is slow. If you open the RemoteApp too early you'll get "Windows File Explorer" because OS registration hasn't finished and it's asking for the location. Wait and retry.

**If assignment fails**: the Nerdio App Service likely lacks Owner on the resource group (see the NME troubleshooting cheat sheet).

*Bron: Nerdio-content 'Troubleshooting' (Troubeshooting).*

## Verwante notities

- [App-V is not dead yet, despite MSIX](app-v-not-dead-yet.md)
- [A six-pillar application management strategy for AVD](avd-application-management-strategy-six-pillars.md)
- [FlexApp One application layering, and how it compares to MSIX](flexapp-one-application-layering-explained.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
- [MSIX AppAttach: what it is and why it matters](msix-appattach-explainer.md)
- [MSIX positioned to replace App-V (2019 transition)](msix-replacing-app-v.md)
- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
- [App layering that keeps the base image clean is the right model for AVD](positie-app-layering-keeps-the-image-clean.md)
