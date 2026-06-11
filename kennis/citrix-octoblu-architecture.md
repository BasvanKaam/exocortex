---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, octoblu, iot, architecture, automation]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Octoblu: an everything-is-a-node IoT platform

How it worked then (2017, Citrix-owned Octoblu): Octoblu 'connects everything to everything' and treats every entity (person, sensor, workflow, service) as a node, each uniquely addressable with a 36-char UUID and accessible via a 32-char token. Workflows add simple logic to automate things, built in a drag-and-drop GUI (Octoblu Designer) that developers can extend with code. It is cloud-based and highly portable across clouds because it runs on node.js inside Docker containers. Five main components: Meshblu (the hub / cross-protocol messaging cop, supporting HTTPS, WebSockets, MQTT, CoAP; also device registry and auth), Octoblu Designer (the GUI), Gateblu (mobile/edge hub connecting smart and not-so-smart devices), Nanocyte (the 24x7 flow automation engine running in secure cloud containers), and Tentacle (formerly Microblu, a microcontroller OS for Arduino-compatible devices). Security cleanly separates authentication from authorisation (a patent-pending system); authz is fully resource-oriented (everything is a resource, white/black-listable per UUID with extensible permissions). ~80% of the stack was open source (800+ GitHub repos). A dated product but a clean example of a node/graph IoT automation model.

*Bron: blogpost 'Citrix Octoblu architectural breakdown' (2017-05-10), basvankaam.com.*

## Verwante notities

- [The Connected Cow: an IoT + cloud big-data use case](connected-cow-iot-bigdata-usecase.md)
- [Docker fundamentals: namespaces, cgroups, images and layers](docker-inner-workings-2015.md)
- [Edge computing and Edge-nodes](edge-computing.md)
- [Firm believer in choice: spread options, but cap the platform count](firm-believer-in-choice-no-one-size-fits-all.md)
- [Honest he's not an IoT developer, but curious about the trajectory](honest-about-not-being-an-iot-developer.md)
- [Industrial IoT will be the biggest sub-vertical (2017 call)](iiot-the-next-big-thing-2017.md)
- [The three-block IoT architecture: Edge, Platform, Enterprise](iot-three-block-architecture.md)
- [Synergy 2015 wish-list: Workspace Cloud, X1, fix the GUIs, better monitoring](stance-synergy-2015-predictions.md)
