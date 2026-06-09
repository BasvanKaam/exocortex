---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [single-user, multi-user, rdsh, fslogix, persistent, gpu]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Single-User vs Multi-User VDI/DaaS

VDI and DaaS can be set up two ways: a VM per user (generally considered the basis of VDI, one of its first applications), or multiple users on one VM.

**Single-user (VM per user):** each user gets a fully isolated, personal desktop with their own OS, apps and settings — more flexibility and customisation, and they can run heavy apps without affecting others. This splits into **persistent** (everything the user changes/installs — files, settings, programs — is retained, like a personal PC) and **non-persistent** (a clean standard desktop each login, reset on logout, no personal changes saved). The downside: single-user machines (persistent or not) need more compute and storage, raising infrastructure and maintenance costs.

**Multi-user (multiple users on one VM):** best compared to a non-persistent machine; enabled via a shared session-hosting architecture like **Remote Desktop Session Host (RDSH)**, called Remote Desktop Services in Windows. Users share a common VM with the same apps and resources. Generally more cost-efficient (less compute/storage per user), best where users don't need extensive personalisation and use similar apps. Downsides: per-user performance can vary (shared resources) and less customisation/isolation. Usually paired with a user-profile solution like **FSLogix** so personal settings (browser favourites, wallpaper, app settings) are stored separately and loaded at login.

Bas from the field: multi-user solutions are by far the most deployed, mainly for cost-efficiency, though it depends heavily on the use case — you often see a mix of both. Exceptions where single-user wins: a developer needs more compute, must install/test apps and reset the VM to its original state (impossible on multi-user without affecting others); and graphics apps for complex design/calculations like CAD software, which need an above-average GPU (Graphical Processing Unit). GPUs increasingly appear in multi-user systems too (compute shared per session) to support common apps like the Office suite — which, though seen as simple, increasingly consume compute, so a GPU relieves the central system.
