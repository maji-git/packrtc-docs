---
weight: 2
title: "Self Hosting"
---

# Self Hosting PackRTC Signaling Server

## Ways to run PackRTC

- [Docker Compose](/docs/signal/self-hosting/docker/) (Recommended)

## Setting PackRTC to use your instance

You can set PackRTC to use your instance by changing `packrtc_url` variable.

```gdscript
# Change PackRTC signaler instance
PackRTC.packrtc_url = "https://your-instance.com"
```