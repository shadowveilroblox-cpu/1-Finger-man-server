ESCAPE 1 FINGER MAN — EDITABLE SOURCE — v1.2.0

All readable game logic, UI and CSS are in maingame.html. Keep this whole folder:
vendor/, textures/, audio/, fonts/, paintings/ and the supplied images are local.
Start a local web server (e.g. python -m http.server 8000), then open
http://localhost:8000/maingame.html. Do not open ES-module games via file://.

NEW IN 1.2.0
- Super Ultra: genuine 4K color, OpenGL-normal and roughness texture maps,
  4096px flashlight shadow maps, stronger SSAO, seven nearby room lights,
  bloom, anti-aliasing and cinematic grading. Very demanding on phones.
  Medium remains the default; High/Ultra and Low remain available.
- Walk on stairs to climb/descend, with continuous height and full control.
  No interaction button and no stair cutscene. Enemy climbs the same staircase.
- Automatic single-player saves every few seconds, on backgrounding, and on
  Save & return to menu. Continue restores the day, location, inventory, opened
  compartments, randomized clues, puzzle flags and enemy position.
- Graphics/audio settings are remembered on this device.
- Online co-op UI and client for 2–4 people, available usernames, rooms joined
  by creator username, shared inventory/puzzles/chances and visible teammates.

IMPORTANT: ONLINE PLAY IS NOT AN ALREADY-HOSTED SERVICE
Deploy the separately included multiplayer server on an HTTPS/WebSocket host
with a persistent writable disk. Every player enters the same server base URL.
Without a deployed server, single-player works but Online explains that it is
not connected. See README-FIRST.txt in the multiplayer-server ZIP.
Creator simulation pauses if the creator disconnects or is backgrounded.
Progress and usernames are stored in that server's SQLite database, not on an
unspecified cloud service. Retain the hosting disk and back it up.

DEVICE SAVE LIMITS
Single-player saves and the username login token are in app/browser storage.
Clearing app/browser data or uninstalling loses them; no account recovery system
is included. A multiplayer username is reserved on its server and a lost token
cannot be recovered through this game. Multiplayer world progress survives
server restarts only when its database disk is preserved.

CONTROLS
WASD/arrows or left joystick: move. Drag screen/mouse: look.
E/hand: interact. C/person icon: crouch. F/bulb: flashlight. Escape: options.
Drawers/cabinets/chests open immediately without search waits. Three drawers per
dresser, hollow trays/chests, visible loot and separate pickup are retained.
Crouch for the initial opening of low floor chests. Inventory button: clues.

PUZZLES
With Extra locks enabled, find red/blue/yellow fuses plus the circuit note,
restore Floor 1 power in its randomized order, unlock the upstairs locker with
its key and four code scraps, and rebuild the knife at the upstairs forge.
Then face the enemy and use the rebuilt knife. Keys, valve, bucket, lava,
forge fuse and accurate strikes are needed. Five chances are shared in co-op.

TESTING / DISTRIBUTION
Browser-tested; not tested on a physical Android device. Public multiplayer has
not been deployed. Updating HTML does not change an installed APK.
All asset credits and licenses are included. No Granny/Grandpa game assets are
copied. The photograph, artwork and app icon were supplied by the user.
