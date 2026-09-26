<div align="center">

<img src="assets/branding/superdummy-icon.png" alt="SuperDummy icon" width="260">

# SuperDummy — 7DTD POI Viewer

### An unofficial, fan-made 3D prefab and POI viewer for 7 Days to Die

Explore game and local prefabs in 3D, create cinematic orbit shots, and save thumbnails for your own projects.

[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows&logoColor=white)](#requirements)
[![Built with Rust](https://img.shields.io/badge/built%20with-Rust-000000?logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Powered by Bevy](https://img.shields.io/badge/powered%20by-Bevy-232326)](https://bevyengine.org/)
[![Project status](https://img.shields.io/badge/status-in%20development-F59E0B)](#project-status)
[![Downloads](https://img.shields.io/github/downloads/xvgray/superdummy-releases/total?label=downloads&color=2EA44F)](https://github.com/xvgray/superdummy-releases/releases)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-support-FFDD00?logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/bullrider)

**[Download 0.1.0 — Water Edition](https://github.com/xvgray/superdummy-releases/releases/tag/v0.1.0)** · [Release notes](https://github.com/xvgray/superdummy-releases/releases/tag/v0.1.0) · [Earlier changelog](CHANGELOG.md) · [Report an issue](https://github.com/xvgray/superdummy-releases/issues) · [Support development](https://buymeacoffee.com/bullrider)

</div>

> **Unofficial project:** SuperDummy — 7DTD POI Viewer is an independent, fan-made tool. It is not affiliated with, endorsed by or supported by The Fun Pimps.

---

## What is SuperDummy?

**SuperDummy — 7DTD POI Viewer** (short name: **SuperDummy**) is a standalone desktop viewer for prefabs and points of interest (POIs) from **7 Days to Die**. It reads compatible prefab data and assets from your existing game installation and builds an interactive 3D scene, making it easier to inspect buildings, block placement and prefab details without loading a game world.

In 7 Days to Die, explorable POIs are built from prefab data. SuperDummy can inspect compatible prefab files whether they represent complete POIs or supporting world-generation elements. In other words, every POI is a prefab, but not every prefab is necessarily a POI.

The application is written in **Rust**, built with **Bevy** and **bevy_egui**, and uses Vulkan rendering on Windows.

## 0.1.0 — Water Edition

Water Edition brings animated water surfaces and refraction, improved terrain transitions, and fixes to materials and lighting. It also adds tools for presenting and previewing your own prefabs.

- **Water preview** — animated surface detail and refraction, with improved shore coverage.
- **Local prefabs** — switch between **GAME PREFABS** and **LOCAL PREFABS**, or choose a custom folder.
- **Prefab thumbnails** — save a clean camera screenshot for a local prefab, with confirmation before replacing an existing image.
- **Cinema orbit** — one full rotation or a continuous loop, selectable direction, and 30 / 60 / 120-second rotations.
- **Tilt-shift** — an optional miniature-style effect during orbit.
- **Fullscreen** — press **F11** to toggle borderless fullscreen.
- **Lamp shadows** — choose a shadow-casting lamp limit of 3, 8 or 12; the default is 8.
- **Built-in Help** — controls, features and practical graphics settings explained inside the application.

[Read the 0.1.0 release notes](https://github.com/xvgray/superdummy-releases/releases/tag/v0.1.0).

## Explore and present

- Navigate with a free-fly camera and inspect prefab geometry and models.
- Surround the POI with generated **Scenic Terrain** for presentation.
- Adjust the time of day, Sun and Moon, exposure, contrast, saturation and gamma.
- Preview prefab lights, animated torches and candles, and PBR materials for blocks, glass, vegetation and terrain.
- Load compatible prefabs using automatic or manual game installation detection and persistent caches.
- Keep application preferences between sessions.

## Requirements

- **Windows 10 or Windows 11**, 64-bit
- A Vulkan-capable graphics card with current drivers
- A legally obtained, compatible installation of **7 Days to Die**
- Enough free disk space for the application and temporary asset data

> Game files and assets are not included with SuperDummy.

## Installation

Download **[SuperDummy 0.1.0 for Windows x64](https://github.com/xvgray/superdummy-releases/releases/download/v0.1.0/SuperDummy-0.1.0-water-edition-windows-x64.zip)**, or visit the [release page](https://github.com/xvgray/superdummy-releases/releases/tag/v0.1.0) for notes and the SHA256 checksum.

1. Extract the **entire ZIP**. Keep the `assets` and `resources` folders beside `superdummy.exe`.
2. Run `superdummy.exe`.
3. The application tries to find your game installation. Select the game folder if prompted.
4. Open **Load POI** and choose **GAME PREFABS** or **LOCAL PREFABS**.

The default local prefab folder is `%APPDATA%\\7DaysToDie\\LocalPrefabs`; you can select another folder in the browser.

**Download the named Windows ZIP, not GitHub's automatic “Source code” archives.** This repository contains public release documentation, not the application source.

Windows SmartScreen may warn about unsigned early builds. Always verify that the archive was downloaded directly from this repository.

## Quick controls

| Action | Where to find it |
| --- | --- |
| Load game or local prefabs | **Load POI** |
| Start an orbit, enable looping or tilt-shift | **Tools → Cinema orbit…** |
| Stop an orbit, including when the interface is hidden | **Esc** |
| Save a thumbnail for the loaded local prefab | **Tools → Save prefab thumbnail…** |
| Toggle fullscreen / windowed mode | **F11** |
| Read the user guide | **Help → User guide** |

Orbit controls camera movement; use an external screen recorder to capture video. Leave enough room around the prefab, as the camera does not avoid obstacles.

Thumbnails are saved as **280 × 210 JPEG** images. Existing thumbnails are replaced only after confirmation. This action is available for local prefabs only.

## Compatibility and performance

**Tested with 7 Days to Die V 3.2.0 (b10), Steam build 24994517.** Other game versions have not been confirmed; detecting an installation does not guarantee compatibility.

- A separate game installation is required. Game assets are not bundled.
- Local prefabs using base-game blocks are supported. Full support for mod-defined blocks and assets is not included.
- Water is a visual approximation, not a fluid simulation. Scenic Terrain is a presentation background, not an exportable game world.
- Higher lamp shadow limits and tilt-shift can reduce frame rate.
- The depth prepass option is experimental and requires an application restart.

## Settings and local data

Settings, logs and caches are stored under `%LOCALAPPDATA%\\SuperDummy`. Preferences are saved in `settings.xml`, independently of the folder from which you launch the application.

When the new settings file does not yet exist, SuperDummy can migrate an older `settings.xml` from beside the executable or from the working directory. The original file is left in place.

## Project status

SuperDummy is under active development. Early releases may contain missing models, fallback geometry, visual differences or compatibility issues after a 7 Days to Die update.

The source code is maintained in a separate private repository. This repository is the official home for public documentation, Windows downloads and release notes.

## A note from the author

Fair warning: SuperDummy has fairly demanding graphics requirements — and, as a
bonus, it looks *worse* than the game it is showing you. The author gives it a
solid 30% and is working hard on making it look even worse. ;)

## Screenshots

The gallery below shows **0.1.0-pre.3**, an earlier build. It does not show all Water Edition improvements.

![SuperDummy v0.1.0-pre.3 displaying a 7 Days to Die POI with presentation lighting and surrounding Scenic Terrain](assets/screenshots/superdummy-pre3-hero.png)

*SuperDummy v0.1.0-pre.3 — a loaded POI with presentation lighting and the
surrounding Scenic Terrain.*

<table>
  <tr>
    <td><img src="assets/screenshots/superdummy-pre3-gallery-1.png" alt="Scene rendered by SuperDummy v0.1.0-pre.3"></td>
    <td><img src="assets/screenshots/superdummy-pre3-gallery-2.png" alt="Scene rendered by SuperDummy v0.1.0-pre.3"></td>
  </tr>
  <tr>
    <td><img src="assets/screenshots/superdummy-pre3-gallery-3.png" alt="Scene rendered by SuperDummy v0.1.0-pre.3"></td>
    <td></td>
  </tr>
</table>

*More scenes rendered by SuperDummy v0.1.0-pre.3.*

## Feedback and bug reports

Suggestions and bug reports are welcome through [GitHub Issues](https://github.com/xvgray/superdummy-releases/issues).

For rendering or loading problems, please include:

- SuperDummy version
- 7 Days to Die version
- Windows version
- Graphics card model
- Name of the affected prefab or POI
- A screenshot and the relevant part of the application log, if available

Please do not attach copyrighted game assets.

## Support the project

If SuperDummy is useful to you and you would like to support its development:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-bullrider-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/bullrider)

Every contribution helps with development, testing and future features. Thank you!

## Disclaimer

SuperDummy — 7DTD POI Viewer is an independent, unofficial fan-made tool. It is not affiliated with, endorsed by or supported by The Fun Pimps or the developers and publishers of 7 Days to Die.

7 Days to Die and related names, trademarks and game assets belong to their respective owners. SuperDummy does not distribute game assets and requires users to provide their own compatible game installation.

## License — Freeware

SuperDummy is distributed as freeware. You may download and use the official application binaries free of charge for personal or commercial purposes, subject to the license terms.

See the full **[SuperDummy Freeware License](LICENSE.md)**.

---

<div align="center">

Made with Rust and Bevy

</div>
