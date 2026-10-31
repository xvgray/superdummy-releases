# SuperDummy 0.2.2 — Forge Edition

**Released 31 October 2026.** Paint, picture mosaics and practical measurements for your prefab workshop.

## Paint and finish your build

- A dedicated **Paint** tab: **Paint, Area, Fill, Mosaic, Pick and Eraser**, with tool symbols, custom cursors and clear outlines of the surfaces that will change.
- **Face / Block** coverage where supported. Block affects all confirmed paintable sides of the chosen blocks.
- **Paint** and **Eraser** work while you drag, show the actual result during the stroke and create one Undo step when you release. Esc cancels the unfinished stroke.
- **Area** offers square, horizontal and vertical stamps, adjustable size and a choice to include separate surfaces. **Fill** follows one connected flat region with a matching finish and stops at gaps, corners and different finishes.
- A starting-plane lock and horizontal/vertical stroke directions help keep paint on the intended wall, floor or ceiling. The eraser has its own size control.
- **Pick** returns to the previously used paint tool after taking a sample. Right click opens a compact settings menu for the current tool.

## Turn a picture into a wall mosaic

Load a local PNG/JPEG and select two corners on a solid vertical wall. Mosaic chooses from the game's existing paints, so the result is ordinary prefab paint data, without a custom-texture mod or the source picture in the game pack.

- The loaded image and thumbnail stay available throughout the program session.
- Compare **Fit / Crop / Stretch**, **Colour / Grayscale**, **Smooth / Sharp / Preserve outlines** and optional gentle colour blending.
- See a prepared preview beside the settings, then apply the whole mosaic as one Undo step.
- Image detail is limited by the number of block faces and the game's palette. Small features and exact colours cannot always be preserved.

## Measure and align

Open **Inspector > Tools > Measurements**:

- **Ruler:** press **R**, then press, drag and release to read a distance and its X/Y/Z spans. Snap to the 1 m grid and keep the result if wanted.
- **Laser level:** **Ctrl+L** places or moves one point with six red axes and metre marks; **Ctrl+Shift+L** clears it.
- **Construction guides:** XZ/XY/YZ reference planes, Auto with axis views, spacing and offsets, main axes and edge rulers. **G** toggles the guides; **L** toggles all measurement helpers.

All three work with perspective and orthographic views. They are session helpers: they are not saved as game blocks or markers.

## Camera, layout and editing fixes

- **Num 1 / 3 / 7** for front/right/top; Ctrl for opposite views; **Num 5** for perspective/orthographic; **Num .** to frame the selection or prefab. Orthographic depth clipping was corrected.
- Save a local prefab to remember its camera view in a small adjacent `NAME.superdummy.json` editor file. It is not required by the game and is not packed into exported mods.
- Inspector tabs are **Block, Markers, Library, Paint and Tools**. Sleeper volumes and road exits are collapsible sections under Markers. **Ctrl+I** reopens the last tab; the chosen panel width is remembered.
- The bottom status bar stays visible across the window.
- Opening a dialog while flying releases the mouse and stops the camera. Closing the dialog leaves pointer mode; use Tab or a fresh middle-button press to fly again.
- Undo/Redo no longer put away the placement tool. A Move/Duplicate grab is safely released if history changes its source. Shape searches in **V** are kept for the session.
- Updated beginner help, tool instructions and shortcuts.

## Updating and first steps

Download **SuperDummy-0.2.2-forge-edition-windows-x64.zip** from Assets and extract the entire archive into a separate folder. Keep **assets** and **resources** beside **superdummy.exe**. No Rust or Bevy installation is needed; GitHub's automatic Source code archives are not the Windows application.

Use **Help > User guide** for the beginner walkthrough, painting and measurement instructions. Existing local prefabs and preferences remain in their own folders.

**Export is optional.** A saved LocalPrefabs building with suitable World placement choices can be considered when generating a new world. Export mainly helps restrict biomes or prepare a mod folder to share; it does not save your working document.

## Requirements and current limits

Windows 10/11 x64, a Vulkan-capable GPU with current drivers, and your own compatible **7 Days to Die** installation. The development baseline is **3.3.0 b18**; game assets are not included.

**Save often and keep separate copies of important work.** There is no emergency autosave or crash recovery. Water editing, mod-added block loading, whole-room move/copy and special mechanisms such as gas valves are not included. Very large prefabs can still load slowly, use substantial memory or become difficult to edit.

Painting is limited to supported game-paintable surfaces. Area/Fill require supported grid-aligned planes; Mosaic requires a solid rectangular vertical wall and uses the existing game paints, not arbitrary new textures. Measurement helpers are not saved between program sessions. Reported application checks cover specific workflows, not every asset, save/failure case or in-game combination. Release preparation does not include a new GUI or game test run.

[Project and screenshots](https://github.com/xvgray/superdummy-releases) · [Report a problem](https://github.com/xvgray/superdummy-releases/issues) · [Roadmap](https://github.com/xvgray/superdummy-releases/blob/main/ROADMAP.md) · [Support development](https://buymeacoffee.com/bullrider)
