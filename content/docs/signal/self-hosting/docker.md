---
weight: 1
title: "Docker Compose"
---

# Self Hosting with Docker Compose

You can use the following Docker Compose as a starting point:

```yaml
version: '3'
services:
  packrtc:
    image: 'mawji/packrtc-signal'
    environment:
      # Port to run PackRTC on
      - 'PORT=3000'
      # Websocket URL for PackRTC (Make sure it doesn't end with slash /)
      - 'PACKRTC_WS=ws://localhost:3000'
```