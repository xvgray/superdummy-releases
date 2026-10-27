# SuperDummy 0.2.1 — editing fixes and usability

Updated **27 October 2026**. **Published: [0.2.1 — Forge Edition](https://github.com/xvgray/superdummy-releases/releases/tag/v0.2.1).**

The scope of this focused patch is closed. The reported editing fixes were checked during development; this does not mean every model, input path or game scenario was tested.

## Included fixes

- [x] Explain missing location tags before saving.
- [x] Fully hide road-exit outlines and helpers when the layer is switched off.
- [x] Hide the last selected sleeper-volume outline with its layer.
- [x] Make attachment to blocks predictable, including thin posts and panels.
- [x] Correct picking of thin/rotated shapes and open doors near other blocks.
- [x] Show a readable amber rotation guide for the actual axis and wheel direction.
- [x] Make Esc cancel the active tool and return to Select; reserve right-click for context menus.
- [x] Make road-exit and sleeper-volume editing independent of block Edit mode, with clearer handles, focused panels and right-click → Edit.
- [x] Add a 254-layer prefab-editor compatibility profile while preserving oversized imports; keep world placement/ground offset distinct.
- [x] Keep the Inspector hidden on Welcome when no document is open.
- [x] Fix blank material-family thumbnails, including the Wood cube.
- [x] Make optional development support easier to find without automatic prompts.
- [x] Add shared Undo/Redo step and memory limits under Settings > General. Expired undo steps retain their effects in saved prefabs.
- [x] Put compact Undo/Redo counters and a detailed tooltip on the bottom status bar, with commands in Tools and existing keyboard shortcuts. The temporary buttons above the Inspector were removed.

## Build and package checks

- [x] Final application/package version is 0.2.1.
- [x] Final compilation and optimized Windows build succeeded, as recorded in the supplied build report and bundled `BUILD_INFO.json`.
- [x] Bundled help was checked against the final history controls and limits.
- [x] Archive integrity and all 44 entries in its internal `SHA256SUMS.txt` were verified.
- [x] ZIP size and SHA-256 match the supplied checksum file.
- [x] Public release notes, changelog and homepage update are prepared, preserving the existing page layout, screenshots and badges.
- [x] Upload both release assets, verify their SHA-256 digests on GitHub and publish v0.2.1 as Latest. The public release page and ZIP link return HTTP 200.

Package: `SuperDummy-0.2.1-forge-edition-windows-x64.zip` — **40,559,522 bytes**.  
SHA-256: `b7010c546564f30ecb324cda637c1b358c567059d29fea23f78db0ca2cea941b`.

## Checks deferred beyond publication

These checks remain open; publication does not count them as passed.

- [ ] Broader targeted save/reload, cancellation and Undo/Redo/Revert all cases after history trimming.
- [ ] A wider matrix of door models, rotations and editing operations.
- [ ] In-game height-boundary trials.
- [ ] Broader large-prefab responsiveness and less common failure/input paths.

No additional GUI, game or automated tests were run during package verification or publication. The build/package checks above are separate from the editing cases checked during development.

## Recovery and later features

Emergency autosave/crash recovery remains planned for a later reliability update with no assigned version. It is not included in this patch. **Save often and keep copies of important work.**

Painting, water editing, mod-added block loading and terrain sculpt remain outside 0.2.1. The [terrain sculpt illustration](ROADMAP.md#terrain-sculpt--an-early-design-for-a-later-release) is an early design for a later release.

[Full roadmap](ROADMAP.md) · [Discuss priorities](https://github.com/xvgray/superdummy-releases/issues/2) · [Report a bug](https://github.com/xvgray/superdummy-releases/issues/new/choose)
