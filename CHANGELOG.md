# Changelog

## V8.4 Stable

### Added

- **Level -1 / Grayscale Halls support** in the existing ESP and radar.
- Ritual targets with required ON/OFF and current light state; correctly configured rooms disappear.
- Ritual progress HUD using runtime completion counts and the game's required-room ratio, plus tutorial progress.
- Active progression TVs, inactive power breakers, Small Keys and locked Small Key doors.
- Final exit marker gated by completed ritual and unlocked exit state.
- Readable SHADOW label using the existing entity/skeleton pipeline; no guessed bone mapping.

### Fixed

- Finished tutorial sectors no longer suggest their remaining rooms as the next ritual targets.
- Inactive TVs and the locked final exit are not shown as available objectives.
- Removed redundant INTERACT prefixes from Level -1 markers.
- State refresh uses cached actors, validates weak-object serials and clears markers on world changes.

Ritual state changes and progress were confirmed in-game. Schema, reader-state and packaging checks passed; the dashboard regression suite passed 33 checks. A complete final-phase playthrough and Shadow skeleton rendering on this level remain unverified. SAFE SWITCH is not included because an active attack state was not reliably established.

Download **BETTrainer.exe** from the release — its runtime DLL is embedded. Restart the trainer after updating; restart the game too if it still has an older runtime loaded. F8 opens the menu; F10 exits.

## V8.3 Stable — 2026-09-14

### Added

- Noclip / Fly in Movement: WASD movement, Space to ascend, Ctrl to descend. Close the trainer menu to use vertical controls.
- Adjustable flight speed from 100 to 5000 uu/s. Profiles save the speed but never automatically enable flight.
- Flight safety reminder: leave walls and descend near the floor before disabling.
- Current level name in the top status bar instead of the game executable name. Process details remain in System diagnostics.

### Fixed

- Reduced flight inertia with speed-scaled acceleration and braking. Original movement and collision settings are restored when flight is disabled or the trainer exits normally.
- Updated GUObjectArray and FNamePool addresses for the September 14 game update.
- Updated and validated the God Mode code-patch signature for that update.

### Verification and compatibility

- User confirmed God Mode, Noclip / Fly and the improved flight braking in-game.
- Release build and embedded runtime packaging checks passed.
- Flight UI/configuration checks passed; flight is not automatically enabled by a saved profile.
- Game executable SHA-256: `3370ddb631ddea09eb8dbc32201ebb29d49081724b69f7f8614fb24cdd569661`.
- Future game updates can require new addresses or code-patch validation. This is not a claim that every feature has been retested on every level.

Distribution remains a single `BETTrainer.exe`. Restart the game and trainer after upgrading to load the matching embedded runtime.

## V8.2 Stable — 2026-09-13

### Added

- **FOV Override** and **Player Field of View** controls in the **Survival** tab.
- Adjustable **30–150°** FOV, including values below the game's 70° minimum and above its 100° maximum.
- FOV settings saved in configuration profiles; older profiles default to override disabled.
- Live camera FOV displayed beside the control.

### Fixed

- FOV now changes the actual player CameraComponent. The tilt modifier's FOV adjustment is disabled while overriding, without disabling head tilt/rotation. Previous settings are restored when the override is disabled or the trainer exits normally.
- Corrected the initial FOV control placement from Movement to Survival.
- Fixed reversed radar arrow rotation when turning left/right.
- Fixed inverted map Y-axis so forward/backward movement agrees with the arrow. Geometry, player position and tracked markers share the same transformation.

### Verification

- Live game checks: requested 60° and 120° produced actual camera values of 60° and 120°; disabling the override restored the original 100°.
- User confirmed FOV and the final radar correction in-game.
- Dashboard regression checks: 33 passed, including arrow/forward-motion agreement across all 360 integer headings.
- FOV slider/config tests cover toggle routing, limits, round-trip saving, invalid numeric input and legacy profile defaults.

Distribution remains **one BETTrainer.exe**, with its matching runtime DLL embedded. BET_OffsetFinder is a separate local utility and is not included in this trainer release.

## V8.1 Stable — 2026-09-13

- Enabled Skeleton ESP for supported entities; removed Test/WIP labels. Clump remains excluded.
- Added purple highlighting for Fuse, Electrical Tape and Wire Bundle on Level 3.
- Updated Object Array, FNamePool and God Mode runtime addresses for the verified game build.
- Embedded the runtime DLL for single-EXE distribution.
