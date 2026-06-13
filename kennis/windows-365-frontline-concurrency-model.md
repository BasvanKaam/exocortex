---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [windows-365, frontline, cloud-pc, daas, licensing]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Windows 365 Frontline: concurrency licensing for shift/frontline workers

Frontline is the next iteration under the Windows 365 umbrella, aimed at frontline/temp workers who only need a Cloud PC occasionally or for part of the day. Feature-wise it matches an Enterprise Cloud PC, with key differences:

- The Cloud PC shuts down when no longer in use, but keeps personal settings and data. Changes persist across shutdown (like an Enterprise Cloud PC). On log-off the user is reminded to save work; forgotten machines can be auto-shut-down.
- Licensing is concurrency-based, not named. You buy licenses only for the number of active employees at any given time. Example: 500 employees but max 150 active concurrently means you need 150 Frontline licenses.
- A license is checked out when a user logs on (machine powers on) and returned to the pool on log-off (machine powers off), fully automated by Microsoft.
- One Frontline license allows up to 3 Cloud PCs to be provisioned for nonconcurrent access by up to 3 users; the extra machines sit powered-down until someone logs on.
- If no license is free, the user (not the admin) is notified at log-on time.
- On cancellation, associated data is retained up to 90 days by default.
- Concurrency is tracked, so admins get historical usage reports to right-size license counts and control cost.
- Intune is the management platform, so no extra infrastructure, admin retraining, or new procedures; apps and config are applied as usual.

Nerdio's License Parking feature for traditional Cloud PCs comes close to what Frontline offers natively. Frontline, Enterprise Cloud PC, and AVD can run side by side; you don't have to pick one.

Target use cases Bas lists: temporary contractors, frontline workers, helpdesk, medical staff, mobile sales force, call center employees.

*Bron: Nerdio-content 'Windows 365 Frontline is now GA' (Blogs).*

## Verwante notities

- [Windows 365 License Optimization: The Three Levers](w365-license-optimization-method.md)
