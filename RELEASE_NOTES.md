# SuperDummy 0.2.1 — Forge Edition

A focused patch for more comfortable prefab editing, with improved selection, placement and controls, plus configurable Undo history.

## Highlights

- **More predictable building:** improved attachment previews, selection of thin and rotated shapes, and targeting of open doors.
- **Clearer rotation and controls:** an amber rotation guide, consistent Esc cancellation and right-click context menus.
- **Better road-exit and sleeper-volume editing:** independent editing sessions, clearer handles and panels, and helpers that disappear when their layers are hidden.
- **Configurable Undo history:** step and memory limits in Settings > General, with compact Undo/Redo counters on the status bar and commands in Tools.
- **Small workflow fixes:** a missing-location reminder before saving, corrected blank Library thumbnails and an Inspector that stays hidden when no prefab is open.

## Undo history

- Configure **Undo steps** (1–1000) and **Memory limit** (16–2048 MB) under **Settings > General > Undo history**. Defaults are 100 steps and 256 MB.
- Undo and Redo share the same budget. The memory limit may reduce the available steps before the step limit is reached.
- Expiring old undo steps does not remove their edits from the prefab or from subsequent saves.
- The status bar shows **Undo: U/L · Redo: R**. Hover for combined usage, estimated memory and the next available operations.
- Use **Tools > Undo/Redo**, **Ctrl+Z**, **Ctrl+Shift+Z** or **Ctrl+Y** in Edit mode.
- After history has been trimmed, **Revert all changes** restores the session's starting state and clears the Undo/Redo window.
- The memory limit covers retained operations only; the document and additional history bookkeeping use memory outside this budget.

## Other changes

- A 254-layer prefab-editor compatibility profile, while preserving oversized imports. This is not a claim of completed in-game height-boundary testing.
- Clearer optional development support, without automatic reminders.
- Updated built-in help for the revised editor workflow.

## Updating

Download **SuperDummy-0.2.1-forge-edition-windows-x64.zip** from this release's Assets section and extract the entire archive into a separate folder. Keep **assets** and **resources** beside **superdummy.exe**.

Your saved local prefabs and preferences remain in their own folders. No Rust or Bevy installation is needed. GitHub's automatic Source code archives are not the Windows application.

## Requirements and limitations

Windows 10/11 x64, a Vulkan-capable GPU with current drivers, and your own compatible 7 Days to Die installation. Game assets are not included.

**Save often and keep separate copies of important work.** Emergency autosave and crash recovery are not included. Painting, water editing, mod-added block loading and region editing remain outside this patch. Very large prefabs can still load slowly or use substantial memory.

The development baseline is **7 Days to Die 3.3.0 b18**. Reported checks cover specific editing cases, not every model, game mechanism or mod.

[Report a problem](https://github.com/xvgray/superdummy-releases/issues) · [Roadmap](https://github.com/xvgray/superdummy-releases/blob/main/ROADMAP.md) · [Support development](https://buymeacoffee.com/bullrider)
