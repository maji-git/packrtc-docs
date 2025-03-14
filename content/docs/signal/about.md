---
weight: 1
title: "Signal Server"
---

# Signal Server

Signal Server is crucial for PackRTC to work. Signaling server keep the state of user's in the game session. Helps passing WebRTC signaling messages.

PackRTC provides a server of it's own, implemented in node.js. The default server is [PackCloud](/docs/signal/packcloud/). However, you can also host your own PackRTC signaler instance. More information [here](/docs/signal/self-hosting/)