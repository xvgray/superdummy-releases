# SuperDummy 0.2.3 — Forge Edition

Build around a 3D reference, reuse entire sections of a prefab and check structural support as you work.

## Added

- **GLB reference models.** In **Inspector > References**, place multiple guides and adjust their position, rotation, opacity and dimensions. Switch between **Textured** and **Solid**. Reference settings are saved in the adjacent `.superdummy.json` editor file. Use **Locate model...** to reconnect a moved GLB. Game exports contain the blockwork.
- **Group editing.** In **Select**, click one block or drag to select a region. Use **Ctrl+C** or **Ctrl+X**, then **Ctrl+V** to preview a copy or move. Turn or tilt a group in 90° steps with the mouse wheel or **Ctrl + wheel**. Each confirmed placement, move or deletion is one Undo step.
- **Structural stability.** Open **View > Structural stability** to see support estimates for blocks and terrain. Optional warnings appear beside the placement preview. Results depend on the editor's ground assumptions.
- **Block health.** Set remaining HP in the Inspector and see the damage state on supported models, including compatible doors.

## Changed

- Shared Studio controls make the Inspector more consistent.
- The Mosaic dialog previews the image before it paints the wall. Large Mosaic and Fill operations show progress while the scene updates.

## Fixed

- Group placement previews stay aligned when the prefab grows. Rotation arrows stay readable from farther away.
- **Esc** cancels an active ruler measurement or laser placement. The **V** picker remembers the last shape category.
- A crash while preparing a light-block preview and unreadable characters in sleeper-volume labels.

## Download and start

Download **[SuperDummy-0.2.3-forge-edition-windows-x64.zip](https://github.com/xvgray/superdummy-releases/releases/download/v0.2.3/SuperDummy-0.2.3-forge-edition-windows-x64.zip)** and extract the entire archive into a new folder. Keep **assets** and **resources** beside **superdummy.exe**, then run the program. Open **Help > User guide** for the walkthrough and tool instructions.

Requires **Windows 10/11 x64**, a Vulkan-capable GPU and your own compatible **7 Days to Die** installation. Keep the GLB source files you reference. Save often and keep separate copies of important work. Emergency crash recovery is still planned.

[Project and screenshots](https://github.com/xvgray/superdummy-releases) · [Full changelog](https://github.com/xvgray/superdummy-releases/blob/v0.2.3/CHANGELOG.md) · [Roadmap](https://github.com/xvgray/superdummy-releases/blob/main/ROADMAP.md) · [Report a problem](https://github.com/xvgray/superdummy-releases/issues)
