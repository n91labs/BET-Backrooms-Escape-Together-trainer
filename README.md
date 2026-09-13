# BET Trainer V8.1 Stable

External trainer and overlay for **Backrooms: Escape Together**.

The trainer attaches to `BETGameSteam-Win64-Shipping.exe`, automatically reconnects after level transitions, and provides survival, movement, flashlight, ESP, radar, objective, LiDAR, and Level 232 economy features.

## Features

### Survival

- God Mode: enemies can see and chase the player but cannot grab or kill them.
- Infinite Stamina.
- Sanity Lock.
- Infinite Downed Blood.
- Disable Fall Damage, automatically suppressed for the required Level 6 story fall.

### Movement and flashlight

- Adjustable movement-speed multiplier.
- Adjustable jump-force multiplier.
- Sprint FOV protection at high movement speeds.
- Adjustable flashlight intensity, range, and cone angle.
- Force Visible mode compatible with the normal flashlight toggle.

### ESP and objectives

- Entities, pickups, quest items, exits, objectives, and interaction points.
- Configurable pickup display distance, labels, distances, and tracers.
- Readable item names instead of internal Blueprint class names.
- Collected pickups and completed objectives are removed automatically.
- Skeleton ESP with an independent toggle for supported entities, including Bacteria, Scratcher and entities on Level FUN and Level 232. Clump remains without skeleton rendering.
- Purple ESP highlighting for Fuse, Electrical Tape and Wire Bundle on Level 3.
- Level-specific support for generators, switches, valves, monitors, puzzle buttons, Level FUN locator arrows, and the red/yellow/green-light HUD.

### Structure map and radar

- Live structure map generated from level geometry.
- Player direction, entities, pickups, exits, and objectives.
- Category filters, zoom, size, and opacity controls.

### Level 6 LiDAR

- Unlimited LiDAR point lifetime for the current session.
- Manual-only LiDAR cloud clearing.

### Level 232 economy

- Detects all currently sellable pickup and grabbable items.
- Displays live dynamic prices directly on ESP.
- Supports demand changes, expired goods, Fire Sale modifiers, and negative prices.
- Highlights the current highest-value items with `[TOP VALUE]`.
- Fire Sale HUD with the live multiplier and remaining seconds.

### Configuration and session safety

- Save, load, and delete configuration profiles.
- Automatic recovery after Hub and level transitions.
- Write features are available in solo sessions or after explicit consent from everyone in the lobby.
- Lobby consent is never stored and must be confirmed again when the roster changes.

## Installation

1. Download `BETTrainer.exe` from the latest GitHub Release.
2. Start **Backrooms: Escape Together**.
3. Launch `BETTrainer.exe`.
4. Press `F8` to open or close the trainer menu.

No additional DLL download is required. The executable includes its matching runtime DLL and automatically extracts it to a private temporary directory when launched. Restart both the game and trainer after upgrading so the game loads the new runtime.

## Compatibility

- Target process: `BETGameSteam-Win64-Shipping.exe`
- Release: V8.1 Stable
- Verified game build: 24285267. Later game updates may require a trainer update.
- Platform: Windows x64

## SHA-256

`DCBD427F33BD2A6571A1353CE0A176981897DC5ACAFED1312FAFA348D64CFEE2`

## Responsible use

Use the trainer only in single-player or in a private lobby where every participant has agreed to its use. Do not use it to disrupt public games or other players.
