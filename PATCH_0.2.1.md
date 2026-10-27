# SuperDummy 0.2.1 — editing fixes and usability

Updated **27 October 2026**. **Scope closed; final implementation in progress.**
**Not released:** the public download is still
[0.2.0 — Forge Edition](https://github.com/xvgray/superdummy-releases/releases/tag/v0.2.0).

The scope of this small patch is now fixed. The reported fixes below have
been checked during development. Configurable Undo limits are the last
implementation in progress; their completion is not assumed in advance.

## Completed in development builds

- [x] Explain missing location tags before saving.
- [x] Fully hide road-exit outlines and helpers when the layer is switched off.
- [x] Hide the last selected sleeper-volume outline with its layer.
- [x] Make attachment to blocks predictable, including thin posts and panels.
- [x] Correct picking of thin/rotated shapes and open doors near other blocks.
- [x] Show a readable amber rotation guide for the actual axis and wheel direction.
- [x] Make Esc cancel the active tool and return to Select; reserve right-click
  for context menus.
- [x] Make road-exit and sleeper-volume editing independent of block Edit mode,
  with clearer handles, focused panels and right-click → Edit.
- [x] Add a 254-layer prefab-editor compatibility profile while preserving
  oversized imports; keep world placement/ground offset distinct.
- [x] Keep the Inspector hidden on Welcome when no document is open.
- [x] Fix blank material-family thumbnails, including the Wood cube.
- [x] Make optional development support easier to find without automatic prompts.

These are development fixes, not features already in the published download.
Checked means the reported editing scope was checked; it does not claim every
model or game scenario was tried. In-game height-boundary trials and broader
compatibility/performance work remain separate.

## Final work within the closed scope

- [ ] **Configurable Undo history — in progress.** Settings will limit the
  retained steps and memory shared by Undo/Redo. Older edits must remain in
  saved prefabs even when their undo steps expire.
- [ ] **Separate history controls — implemented, pending integration checks.**
  Undo/Redo have been moved above the Inspector, with a right-edge fallback
  when it is closed. The combined check/build is waiting for the ongoing
  history implementation; appearance has not yet been checked.

## Release preparation

- [ ] Verify save/reload, Undo/Redo/Revert all and cancellation after history changes.
- [ ] Complete a successful final compilation and release build.
- [ ] Update the version, changelog and guide for the delivered scope.
- [ ] Review the changes, prepare the package and publish the verified downloads.

There is no release date yet. Closing the scope does not mean a 0.2.1 release,
source push or download update has already happened.

## Recovery and later features

Emergency autosave/crash recovery remains planned for a later reliability
update with no assigned version. It is not included in this patch.
**Save often and keep copies of important work.**

Painting, water editing, mod-added block loading and terrain sculpt remain
outside 0.2.1. The [terrain sculpt illustration](ROADMAP.md#terrain-sculpt--an-early-design-for-a-later-release)
is an early design for a later release.

[Full roadmap](ROADMAP.md) · [Discuss priorities](https://github.com/xvgray/superdummy-releases/issues/2) · [Report a bug](https://github.com/xvgray/superdummy-releases/issues/new/choose)
