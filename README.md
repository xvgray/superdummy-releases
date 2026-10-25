<div align="center">

<img src="assets/branding/superdummy-icon.png" alt="SuperDummy icon" width="240">

# SuperDummy

**0.2.0 — Forge Edition**

*From viewing to creating.*

A free, standalone prefab editor and inspection tool for **7 Days to Die**.

Build a new POI, edit an existing one, configure supported doors, lights and sleeper areas, and save it for use in the game. You can also explore and present prefabs without launching a game world.

[![Download for Windows](https://img.shields.io/badge/Download%20for%20Windows-0.2.0%20x64-2EA44F?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/xvgray/superdummy-releases/releases/download/v0.2.0/SuperDummy-0.2.0-forge-edition-windows-x64.zip)

[Release notes](https://github.com/xvgray/superdummy-releases/releases/tag/v0.2.0) · [What can you do with SuperDummy?](#what-can-you-do-with-superdummy) · [Report an issue](https://github.com/xvgray/superdummy-releases/issues) · [Support development](https://buymeacoffee.com/bullrider)

**Windows 10/11, 64-bit · Requires your own 7 Days to Die installation · No game assets included**

</div>

---

## Screenshots

*Earlier screenshots from **SuperDummy 0.1.0 — Water Edition**, showing the preview and presentation tools. The new editing features are described below.*

![SuperDummy 0.1.0 — Water Edition displaying a 7 Days to Die POI with presentation lighting and surrounding Scenic Terrain](assets/screenshots/0.1.0/superdummy-0.1.0-hero.png)

<table>
  <tr>
    <td><img src="assets/screenshots/0.1.0/superdummy-0.1.0-gallery-1.png" alt="Scene rendered by SuperDummy 0.1.0"></td>
    <td><img src="assets/screenshots/0.1.0/superdummy-0.1.0-gallery-2.png" alt="Scene rendered by SuperDummy 0.1.0"></td>
  </tr>
  <tr>
    <td><img src="assets/screenshots/0.1.0/superdummy-0.1.0-blocks-hidden.png" alt="SuperDummy 0.1.0 with prefab blocks hidden"></td>
    <td><img src="assets/screenshots/0.1.0/superdummy-0.1.0-sleeper-statistics.png" alt="SuperDummy 0.1.0 sleeper statistics panel"></td>
  </tr>
</table>

*More views rendered by SuperDummy 0.1.0, including a blocks-hidden view and the sleeper statistics panel.*

---

## What can you do with SuperDummy?

- **Build a new prefab** — start empty or with flat ground, choose blocks and variants, and grow the workspace as you build.
- **Edit individual objects** — Select, Move, Duplicate, Pick, Insert, Delete and rotate, with previews and Undo/Redo. Supported multiblock objects move together.
- **Find your building parts** — use the block Library, Quick Blocks and separate visibility controls for Player and developer blocks.
- **Set supported object states** — open or close non-powered doors, shutters, hatches and gates, set their locks, switch supported lamps and edit supported writable signs.
- **Prepare gameplay and placement** — edit the supplied basic sleeper-volume/group tools, choose world locations, set ground level and author road-exit markers.
- **Save and return to your work** — Save/Save As, saved-state feedback and prompts for unsaved changes.
- **Inspect and present POIs** — browse game/local prefabs, fly through the scene, read POI and sleeper statistics, export TXT/CSV reports, use cinema orbit and save thumbnails.
- **Optionally restrict biomes or share a pack** — Export for game creates a ready-to-copy mod folder. It is not required for the game to find a saved local prefab.

SuperDummy is an editor and preview tool, not a game client. It does not simulate enemy AI, structural collapse, electrical networks or the full world generator.

## What's new in 0.2.0 — Forge Edition

**From viewing to creating.** Create and edit prefabs, use the block Library and Quick Blocks, adjust supported doors and lights, configure basic sleeper areas, choose world locations and create road connections. Save your work locally and check it in the game.

This release also adds optional biome-aware mod-pack export, clearer installation instructions and a beginner's **Your first prefab** guide. It fixes affected window frame/glass materials, supported door geometry, saved-frame bounds and the half-block offset of chain-link rail previews.

[Read the full 0.2.0 release notes](https://github.com/xvgray/superdummy-releases/releases/tag/v0.2.0) · [Changelog](CHANGELOG.md)

## Installation and first run

1. Download **[SuperDummy 0.2.0 for Windows x64](https://github.com/xvgray/superdummy-releases/releases/download/v0.2.0/SuperDummy-0.2.0-forge-edition-windows-x64.zip)** and extract the **entire ZIP**.
2. Keep the `assets` and `resources` folders beside `superdummy.exe`.
3. Run `superdummy.exe`. SuperDummy tries to find your game installation; select the game folder if prompted.
4. Choose **New Prefab…** to start building, or **Load POI…** to open an existing prefab.
5. Open **Help > User guide > Your first prefab** for a complete beginner walkthrough. **Tab** switches between the pointer and camera control; **Ctrl+S** saves your work.

The default local prefab folder is `%APPDATA%\7DaysToDie\LocalPrefabs`; you can choose another folder in the browser. Settings, logs and caches are stored in `%LOCALAPPDATA%\SuperDummy` (preferences in `settings.xml`).

> **Download the named Windows ZIP, not GitHub's automatic “Source code” archives.** This repository contains public release documentation, not the application source.

## Use your prefab in a new world — export is optional

1. Open **Tools > Prefab Settings…**, choose a suitable location and press **OK**. For a first isolated house, **Outside settlements** is a simple choice.
2. Press **Ctrl+S** and save in the game's **LocalPrefabs** folder, normally `%APPDATA%\7DaysToDie\LocalPrefabs`. Keep the `.tts`, `.blocks.nim` and `.xml` together.
3. Restart the game and generate a **new** world. The generator can consider your building when a suitable place is available. Placement is not guaranteed, and existing worlds are not rebuilt.

**You do not need to export or create a mod just to make a local prefab available.** Use **File > Export for game…** mainly to limit it to selected biomes, such as Forest and Snow, or to prepare a mod folder to share.

A **location** describes a kind of place, such as Outside settlements or Residential district. A **biome** describes the landscape, such as Forest or Snow. Biome choices alone do not make a building available. **Export includes a copy of your edits but does not save the working document — use Ctrl+S too.**

Check **View > Ground Level** before a game trial. Use **Tools > Set Ground Level…** if the building meets the world terrain at the wrong height. Road-exit markers can request a wilderness approach; several markers give the generator a choice, not a promise of several roads.

## Requirements, compatibility and limitations

**Requirements**

- **Windows 10/11, 64-bit**, with a Vulkan-capable GPU and current drivers.
- **8 GB RAM minimum; 16 GB recommended.**
- Your own, compatible installation of **7 Days to Die**. Game files and assets are not included.

**Development baseline and reported game checks: 7 Days to Die V 3.3.0 (b18).** The user checked the reported editing cases and generated POIs with corrected ground level and road connections. This is not exhaustive verification of every model, mod or placement rule. Detecting an installation alone does not prove compatibility.

**Limitations**

- Local prefabs are based on the base game's blocks. Blocks and assets added by mods are **not fully supported**; a mod-dependent prefab may render with missing parts.
- SuperDummy does not simulate AI, structural collapse, electrical networks or actual spawn behaviour. Sleeper previews do not predict the exact enemies spawned.
- Powered-device editing and the elevator test door profile are outside the non-powered door workflow.
- Water editing, region/group building tools and crash recovery are not added in 0.2. Save regularly and keep copies of important work.
- Some separate canvas-sign libraries have explicit save restrictions. Export does not generate distant `.mesh` / `.ins` files.
- Modded world-placement rule order is not fully analysed; reported Forest/Snow placement is not exhaustive proof of exclusion from other biomes.
- Water is a **visual approximation**, not a fluid simulation.
- **Scenic Terrain** is a presentation background, not an exportable game world.
- **Cinema orbit** controls the camera only; recording a video requires an external screen recorder.
- Thumbnails are **280 × 210 JPEG** images and are available for **local prefabs** only.
- Higher lamp shadow limits and tilt-shift can reduce the frame rate. The depth prepass option is experimental and requires a restart.

## Feedback, bugs and ideas

Suggestions and bug reports are welcome through [GitHub Issues](https://github.com/xvgray/superdummy-releases/issues).

Please include:

- the **name of the affected prefab or POI**,
- your **SuperDummy version** and **7 Days to Die version**.

For technical problems, also add:

- your **Windows version** and **graphics card**,
- a **screenshot** and the relevant part of the application **log**.

Please **do not upload or attach game assets**.

If SuperDummy saved you time, a ⭐ on the repository is a simple way to say thanks.

## Project status

The latest release is **0.2.0 — Forge Edition**, bringing prefab editing alongside the existing viewing and presentation tools. The project is **still under active development**. Reported manual checks cover particular workflows; they do not promise full compatibility with every game asset, mod or version.

The source code is maintained in a separate private repository. This repository is the official home for public documentation, Windows downloads and release notes.

## Support the project

If SuperDummy is useful to you, you can support its development:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-bullrider-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/bullrider)

Every contribution helps with development, testing and future features. Thank you!

## License — Freeware

SuperDummy is distributed as freeware for personal or commercial use, subject to the license terms. See the full **[SuperDummy Freeware License](LICENSE.md)**.

## Disclaimer

SuperDummy is an independent, unofficial fan-made tool. It is not affiliated with, endorsed by or supported by The Fun Pimps or the developers and publishers of 7 Days to Die. 7 Days to Die and related names, trademarks and game assets belong to their respective owners. SuperDummy does not distribute game assets and requires users to provide their own compatible installation.

---

<div align="center">

Made with Rust and Bevy

</div>
