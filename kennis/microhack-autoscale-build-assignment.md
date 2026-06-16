---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [idee, nerdio, avd, autoscale, microhack, assessment, host-pool]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# MicroHack assignment: AVD autoscale build spec

The scored build challenge I use to close an Innovation Day. Learners configure a full autoscale profile but deliberately do NOT enable it (so nothing actually spins up and bills). It doubles as a competency check across every autoscale lever. Spec as used early 2024.

## The brief
Build a hostpool and set up Auto-Scale, but do NOT enable autoscale.

- Multi-Session hostpool on Standard D2s_v5, plus the day's other defaults.
- Disks: Running Disk = Premium SSD, Stopped Disk = Standard HDD.
- 4 hosts with CPU Usage Scaling Logic enabled (base host pool). No Scale-in Restrictions.
- Capacity: 1 machine on all the time, 2 machines as Burst capacity.
- Rolling Drain Mode window for 50% of machines at 14:00.
- Pre-stage 2 machines at 7AM Mon-Fri, set correct time zone, exclude from autoscale for 1 hour.
- Enable Auto-Heal Broken Hosts: restart machine once, 10-minute interval, then recreate.
- Save and close - do NOT enable autoscale.
- Hostpool properties: deploy VMs across all Availability Zones; FSLogix must not be used.
- Hostpool properties: log off disconnected sessions after 2 hours.

## Why it works as assessment
Every line maps to a distinct Nerdio autoscale control (scaling logic, burst capacity, drain windows, pre-staging with autoscale exclusion, auto-heal, AZ spread, session timeouts). Getting all of them right proves the learner can operate the full profile, not just click through a wizard. The "do not enable" rule keeps a shared lab tenant from running up cost.

*Bron: Nerdio-content 'Innovation Day hands-on labs' (Innovation Days).*

## Verwante notities

- [The Innovation Day / MicroHack hands-on event format](nerdio-innovation-day-microhack-format.md)
