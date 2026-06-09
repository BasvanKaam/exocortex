---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [session-reliability, cgp, xte-service, auto-client-reconnect, keep-alive]
layer: reference
bron: inside-citrix-fma
---

# Session Reliability, Auto Client Reconnect and ICA Keep-Alive

When Session Reliability (SR) is enabled, the ICA Client tunnels ICA traffic inside the Common Gateway Protocol (CGP) to port 2598 instead of 1494. The **XTE service** acts as a relay, removing the CGP layer and forwarding traffic to the ICA listener on port 1494 internally (and vice versa for server-to-client traffic).

SR buffers ICA traffic when the CGP connection breaks, temporarily storing data until the connection is restored. While buffering, the session stays active on the server (not disconnected); from the client it looks frozen while reconnecting. Once restored, buffered data is flushed and the session continues.

By default SR is configured via policy and set to 180 seconds (3 minutes) before the session is dropped to disconnected; the timeframe and the default port (2598) are configurable. With SR enabled, users auto-reconnect without re-authenticating, unless you set the 'Auto client reconnect authentication' policy to prompt.

**Auto Client Reconnect** detects unintended disconnected ICA sessions and reconnects automatically. If both SR and Auto Client Reconnect are used they work in sequence: SR applies first, and when the SR timeframe elapses and the session disconnects, Auto Client Reconnect kicks in.

As an alternative to SR you can configure **ICA Keep-Alive**, which sends a constant stream of ICA packets every few seconds to detect if the session is active before marking it disconnected. In practice SR is almost always preferred over ICA Keep-Alive.
