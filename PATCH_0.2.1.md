# SuperDummy 0.2.1 — editing fixes and usability

Updated **26 October 2026**. **Planned / in progress — not released.**
The current public download is still **[0.2.0 — Forge Edition](https://github.com/xvgray/superdummy-releases/releases/tag/v0.2.0)**.

This patch is based on problems found while building with 0.2.0. I'm working
through them one step at a time, checking each change during development. The list
below records progress, not a promise that an unfinished fix is already in
your download.

## The checklist, in working order

| Step | What should improve | Current status |
| --- | --- | --- |
| 1. Saving without tags | Explain missing location tags before saving; offer location settings or an explicit choice to save a draft without tags. | Implemented in development builds. The warning has been checked; remaining save/cancel flows still need review. Not released. |
| 2a. Hide road exits fully | Turning the layer off also hides the last selection, circle, center and handles. Hidden helpers must not intercept clicks. | Fixed in development builds. Checked that the outlines disappear when switched off (26 October). Not released. |
| 2b. Hide sleeper volumes fully | Turning the layer off also hides the selected volume, without an extra click in the scene. | Fixed in development builds. Checked that the selected outline disappears when switched off (26 October). Not released. |
| 3. Place blocks more easily | Show the attachment face/plane, including on thin posts and panels; keep targeting, ghost and placement consistent. | In progress. Implementation and visual checks are not complete yet. |
| 4. Select visible objects reliably | Improve picking difficult objects, especially open door leaves outside their original footprint. | Reported; not started. |
| 5. Show rotation direction | Display a clear arrow/arc for the actual rotation axis and direction, matching the preview and final result. | Planned; not started. |
| 6. Consistent right-click and Esc | Use right-click for context menus. Esc cancels the active edit safely and returns to Select when leaving the tool. | Planned; not started. |
| 7. Easier area handles | Make road-exit and sleeper-volume edges/handles easier to discover and drag; retain numeric fields for precise values. | Planned; not started. Existing road-exit Move/Resize tools will be refined. |
| 8. Check height limits | Establish the game's real world/prefab height limits, show clear bounds and prevent edits outside the supported range. | Source/data research completed for 3.3 b18. Editing restrictions and in-game boundary checks are not started; different mechanisms have different limits. |
| 9. Blank library previews | Prevent an empty frame from being kept as a finished material-family thumbnail, especially Wood; avoid duplicate preview requests. | Fixed in development builds. Checked that the Wood cube preview appears correctly instead of an empty dark tile (26 October). Other families and category/prefab-switching checks remain pending. Not released. |

The two original visibility symptoms have been checked during development:
outlines disappear after switching off their layers. This does not yet confirm hidden-hit
handling, cancelling an active drag, restoring drafts/selection, independent
switches or thumbnail suppression. Those remain review items. All fixes are
local and unreleased.

Placement and selection may share technical causes, but both reported
workflows must be checked separately.

For height limits, we first need to distinguish the world ceiling, prefab file
height and placement/ground offset. Any restrictions must follow the game data
and code, preserve imported content and explain why an operation is refused.

## Before publishing 0.2.1

- [ ] Finish the listed fixes and development checks, or clearly state which items
  move to a later release.
- [ ] Check save/reload, Undo/Redo and cancellation for the changed workflows.
- [ ] Complete the final compilation/release build after the last code change.
- [ ] Update the user guide, version and changelog for the actual delivered scope.
- [ ] Review the source changes, prepare the release package and verify public
  downloads when publication is requested.

There is no release date yet. Compiling a fix does not prove that its controls
or appearance work correctly. The current progress does not mean a 0.2.1
release or source push has already happened.

## What happens to recovery?

The earlier roadmap assigned session recovery to 0.2.1. The immediate priority
has now changed to this focused patch. **Recovery remains planned for a later
reliability update; its release number is not assigned yet.** It is not being
silently dropped or claimed as part of this patch. The current application
still has no emergency autosave or crash recovery: save often and keep copies.

Painting, water editing, mod-added block loading and other major extensions
are outside this patch. The later roadmap targets remain unchanged.

[Full roadmap](ROADMAP.md) · [Discuss priorities](https://github.com/xvgray/superdummy-releases/issues/2) · [Report a bug](https://github.com/xvgray/superdummy-releases/issues/new/choose)
