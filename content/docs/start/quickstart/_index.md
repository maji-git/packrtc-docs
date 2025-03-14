---
weight: 2
title: "Quickstart"
---

# Quickstart Guide

1. Install PackRTC from Godot AssetLib

2. Enable PackRTC Plugin (Project -> Project Settings -> Plugins)

![Project Settings -> Plugins](image.png)

3. Set `PackRTC.game_channel` variable to your own unique name (like your game name, hashes)

```gdscript
PackRTC.game_channel = "the_game_name"
```

4. In your multiplayer script, host by using this following snippet (adjust as needed)

```gdscript
var session = await PackRTC.host()
if session is PRSession:
	await session.peer_ready
	multiplayer.multiplayer_peer = session.rtc_peer
	print("Code: ", session.code)
else:
	print("Error: ", session)
```

5. For joining, use `PackRTC.join(code)`

```gdscript
var session = await PackRTC.join(code)
if session is PRSession:
	await session.peer_ready
	multiplayer.multiplayer_peer = session.rtc_peer
	print("Peer Ready!")
else:
	print("Error: ", session)
```