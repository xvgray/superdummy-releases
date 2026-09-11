<div align="center">

<img src="assets/branding/superdummy-icon.png" alt="SuperDummy icon" width="260">

# SuperDummy — 7DTD POI Viewer

### An unofficial, fan-made 3D prefab and POI viewer for 7 Days to Die

Explore prefabs and points of interest outside the game with a free-fly camera and configurable real-time rendering.

[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows&logoColor=white)](#requirements)
[![Built with Rust](https://img.shields.io/badge/built%20with-Rust-000000?logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Powered by Bevy](https://img.shields.io/badge/powered%20by-Bevy-232326)](https://bevyengine.org/)
[![Project status](https://img.shields.io/badge/status-in%20development-F59E0B)](#project-status)
[![Downloads](https://img.shields.io/github/downloads/xvgray/superdummy-releases/total?label=downloads&color=2EA44F)](https://github.com/xvgray/superdummy-releases/releases)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-support-FFDD00?logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/bullrider)

**[Download the latest release](https://github.com/xvgray/superdummy-releases/releases/latest)** · [Changelog](CHANGELOG.md) · [Report an issue](https://github.com/xvgray/superdummy-releases/issues) · [Support development](https://buymeacoffee.com/bullrider)

</div>

> **Unofficial project:** SuperDummy — 7DTD POI Viewer is an independent, fan-made tool. It is not affiliated with, endorsed by or supported by The Fun Pimps.

---

## What is SuperDummy?

**SuperDummy — 7DTD POI Viewer** (short name: **SuperDummy**) is a standalone desktop viewer for prefabs and points of interest (POIs) from **7 Days to Die**. It reads compatible prefab data and assets from your existing game installation and builds an interactive 3D scene, making it easier to inspect buildings, block placement and prefab details without loading a game world.

In 7 Days to Die, explorable POIs are built from prefab data. SuperDummy can inspect compatible prefab files whether they represent complete POIs or supporting world-generation elements. In other words, every POI is a prefab, but not every prefab is necessarily a POI.

The application is written in **Rust**, built with **Bevy** and **bevy_egui**, and uses Vulkan rendering on Windows.

## What's new in pre.3

- **Scenic Terrain** — a generated 512 × 512 m landscape (hills, mountains, rocks
  and snow) that surrounds the loaded POI.
- A dynamic **day–night cycle** with a moving Sun and Moon, twilight, stars and a
  night sky.
- Native **prefab Point/Spot lights**, lamp controls, optional lamp shadows and
  animated torches and candles.
- Improved **PBR materials** for block geometry, glass, vegetation and terrain.
- New **image settings** (exposure, contrast, saturation, gamma) and shadow
  quality levels.
- Reliable **game installation detection** across all Steam drives, plus a manual
  folder picker.
- Much **faster POI loading** through caching and a reworked loader.

See the [changelog](CHANGELOG.md) for the full list.

## Features

- Explore 7 Days to Die prefabs and POIs in an interactive 3D view
- **Scenic Terrain** — a generated landscape that surrounds the loaded POI as a
  presentation background
- A dynamic **time of day** — a moving Sun and Moon, twilight, stars and a night
  sky
- Native **prefab lights** (Point and Spot) with lamp controls and lamp shadows
- Modern **PBR materials** for blocks, glass, vegetation and terrain
- New **image settings** — exposure, contrast, saturation and gamma
- Automatic and manual **game installation** detection
- Staged, responsive loading with persistent caches
- Navigate freely with a fly camera
- Build geometry from block and prefab data
- Display block models from your game installation
- Save application preferences
- Read compatible XML, `.blocks.nim` and `.tts` data

## Requirements

- **Windows 10 or Windows 11**, 64-bit
- A Vulkan-capable graphics card with current drivers
- A legally obtained, compatible installation of **7 Days to Die**
- Enough free disk space for the application and temporary asset data

> Game files and assets are not included with SuperDummy.

## Installation

The latest public Windows archive is available on the [Releases](https://github.com/xvgray/superdummy-releases/releases) page.

To install SuperDummy:

1. Download the ZIP archive attached to the newest release.
2. Extract it to a writable folder and keep the `assets` and `resources` folders
   next to `superdummy.exe`.
3. Run `superdummy.exe`.
4. SuperDummy automatically finds your 7 Days to Die installation through Steam,
   including libraries on other drives.
5. If detection fails, choose your 7 Days to Die folder in the **Game
   installation** window.
6. Click **Load POI** and select a prefab.

Windows SmartScreen may warn about unsigned early builds. Always verify that the archive was downloaded directly from this repository.

## Project status

SuperDummy is under active development. Early releases may contain missing models, fallback geometry, visual differences or compatibility issues after a 7 Days to Die update.

The source code is maintained in a separate private repository. This repository is the official home for public documentation, Windows downloads and release notes.

## Screenshots

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
