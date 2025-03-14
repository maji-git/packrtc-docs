---
weight: 2
title: "Quickstart"
---

# Quickstart Guide

1. Install PackRTC from Godot AssetLib

2. Enable PackRTC Plugin (Project -> Project Settings -> Plugins)

![Project Settings -> Plugins](image.png)

3. In your multiplayer script, host by using this following snippet (adjust as needed)

```gdscript
var session = await PackRTC.host()
if session is PRSession:
	await session.peer_ready
	multiplayer.multiplayer_peer = session.rtc_peer
	print("Code: ", session.code)
else:
	print("Error: ", session)
```

4. For joining, use `PackRTC.join(code)`

```gdscript
var session = await PackRTC.join(code)
if session is PRSession:
	await session.peer_ready
	multiplayer.multiplayer_peer = session.rtc_peer
	print("Peer Ready!")
else:
	print("Error: ", session)
```