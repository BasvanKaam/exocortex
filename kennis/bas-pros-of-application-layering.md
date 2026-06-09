---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [bas-opinion, application-layering, appdisks, app-volumes]
layer: rich
bron: inside-citrix-fma
---

# Bas on the pros of application layering

Bas acknowledges the cons people raise (another product/GUI on the stack, cost, no app isolation) but argues they're soon forgotten given the pros. On the counterarguments: learning to create/assign/update layers takes only a couple of hours max; if you're a VMware or Citrix shop, App Volumes or AppDisks integrate with minimal stack impact ('who cares about another GUI if it helps you solve some major issues'); and lack of isolation can be an advantage since apps that can't be virtualised usually have a reason, and interacting with the underlying OS can help.

His pro list: no more apps in the base image (bar a few of your choosing); possibly just one or two golden images; apps managed independently per layer, even on different schedules or on the fly without impacting production; works for drivers, add-ons and plug-ins; depending on technology, apps appear/disappear dynamically without logout/reboot; leverages Active Directory for assignment; makes non-persistent desktops more achievable; supports all major hypervisors, RDSH and VDI platforms; combined with a personal data/AppDisk you can get persistent-desktop benefits while keeping non-persistent advantages; most products include application lifecycle management; reduces storage, compute, network costs and packaging/provisioning time.

He stresses layering and app virtualisation go hand-in-hand, and that layering is easy and easily delegated to other teams, unlike App-V packaging which 'can be an art on its own.'
