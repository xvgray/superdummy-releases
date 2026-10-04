# Changelog

All notable changes to SuperDummy will be documented in this file.

SuperDummy 0.1.0 — Water Edition is the first stable release. The project remains under active development, and features or behaviour may still change in future releases.

## [Unreleased]

Nothing yet.

## [0.1.0] - 2026-09-26

First stable release — **Water Edition**, following the three 0.1.0 previews.

### Added

- Static prefab water preview with animated procedural ripples, screen-space refraction and an independent `View → Water` toggle
- `GAME PREFABS` / `LOCAL PREFABS` browser modes, with a configurable local prefab folder
- Local prefab thumbnail capture: a clean 280 × 210 JPEG camera view, with confirmation before replacing an existing image
- Cinema orbit with single or looping rotations, selectable direction, 30 / 60 / 120-second durations and an optional hidden interface
- Optional tilt-shift presentation effect during cinema orbit
- Borderless fullscreen through `F11` or `View → Fullscreen`, including during cinema orbit
- Bundled user guide under `Help → User guide`
- POI statistics with TXT/CSV export and sleeper statistics
- Experimental depth prepass setting, disabled by default and applied after a restart

### Changed

- Improved water shore coverage and terrain transitions
- Improved vegetation transparency, glass, screen lighting, and animated torch and candle presentation
- Lamp shadow limits of 3, 8 or 12 nearby shadow-casting lamps, with 8 as the default
- Settings now use `%LOCALAPPDATA%\SuperDummy\settings.xml`, with one-time migration from older locations and a backup of corrupt settings files
- Runtime assets and Help are located relative to the executable, so the package can be launched from another working directory

### Known limitations

- Water remains a static visual approximation: fluid simulation, flow masks, foam, underwater effects and water collision are not reproduced
- Mod-defined blocks and assets are not fully supported; local prefabs still use assets from the user's base-game installation
- Scenic Terrain is presentation scenery, without world streaming or collision
- Tested with 7 Days to Die V 3.2.0 (b10), Steam build 24994517; other versions have not been verified
- Large POIs, higher lamp shadow limits and tilt-shift can increase resource use or reduce frame rate

## [0.1.0-pre.3] - 2026-09-11

### Added

- Dynamic time-of-day system with animated Sun and Moon, twilight, stars and a night sky
- Optional time animation with 1x, 10x, 60x and 300x speeds, plus an on-screen clock
- **Scenic Terrain** (`Ground → Terrain`): a deterministic 512 × 512 m generated landscape around the loaded POI
- Natural ground material for the generated terrain (forest ground, with topsoil and dirt fallbacks)
- Valley floors that fill open terrain gaps inside a prefab, such as the space under a broken bridge
- New image settings: exposure, contrast, saturation and gamma, with a reset button
- Directional shadow-quality levels: `None`, `Some` and `Full`
- Native prefab Point and Spot lights parsed from Unity data, with lamp controls
- Optional lamp shadows, with a budget of up to three nearby shadow-casting prefab lights
- Animated torch and candle lighting
- Automatic game-installation discovery across all Steam libraries and drives
- Manual game-folder picker for custom installations
- `Settings → General → Game installation` section showing and changing the active folder
- Separate sky pass so the sky no longer feeds Bloom
- Correct window, taskbar and Alt+Tab icon

### Changed

- Bloom strength levels and an independent Sun-halo switch
- Reorganized Settings into General, Graphics, Lighting, Time, Controls and Diagnostics
- Reworked the POI loader with staged, responsive loading
- Corrected ambient-light ownership and recalibrated daytime ambient lighting

### Fixed

- More stable rendering of some POIs (an invalid anisotropic sampler combination could terminate the renderer)
- Excessive self-illumination on opaque ShapeNew materials
- Anisotropic texture samplers now always use linear filters (a wgpu requirement)
- Support for Unity `TypelessData` buffers larger than 1 MB
- The inactive Sun or Moon no longer performs directional shadow work
- Restored block placeholder resolution for supported prefab content

### Performance

- Added an LRU cache for decompressed Unity bundles with a configurable memory budget
- Persistent PrefabTree, prepared-texture and collider-mesh caches with source invalidation
- Persistent negative collider cache for known-unsupported local collider meshes
- Native GPU upload for BC1, BC3 and BC7 textures instead of CPU decoding
- `Game/Entity Tint Mask` moved from CPU texture baking to the GPU
- Staged loading keeps the interface responsive during POI preparation
- `bus_stop_01` warm load reduced from ~23 s to ~4 s (depends on the POI, hardware, storage and cache)

### Known limitations

- Early preview: not every 7DTD material, terrain or prefab behaviour is reproduced yet
- Large and complex POIs can still use a lot of memory and run at low frame rates
- Scenic Terrain is generated presentation scenery — it is not the real 7DTD world, is finite, and has no collision or streaming
- Directional shadow-quality changes require an application restart
- Automatic installation discovery targets Steam; other or portable installations use the folder picker
- Volumetric fog is not available in pre.3

## [0.1.0-pre.2] - 2026-09-04

### Added

- Experimental Transvoxel-based prefab terrain rendering
- TTS density parsing and correct density-to-block pairing after the Z-axis coordinate conversion
- `PoiGrid` terrain representation and density lookup
- Terrain diagnostics, real POI scans and density histograms
- Fixed-point terrain vertex interpolation and generated terrain normals
- Worker-thread terrain generation
- Terrain textures with top and side material resolution
- Diffuse terrain textures loaded from `terraintextures_assets_all.bundle`
- World-space terrain texture mapping and three-texture blending
- Initial DistantDecoTree and vegetation support
- SpeedTree UV and material support
- Alpha-cutout foliage rendering
- View menu toggles for Terrain, Shape Blocks, Props and Trees
- `Show All` view reset
- Lighting presets: Editor, Sunny, Overcast and Golden Hour
- Fog modes: Off, Atmospheric and Volumetric
- Native GPU upload for BC1, BC3 and BC7 textures
- Complete texture mipmap chains instead of loading only mip level 0
- Correct Linear and sRGB texture handling based on Unity `m_ColorSpace`
- RGBA texture fallback when native BC upload is unavailable
- Complete POI loading-time measurement, covering preparation through the final scene swap
- Optional FPS counter available under `Settings → Graphics → Show FPS counter`
- Persistent FPS counter setting
- Regression tests for terrain placement at voxel and grid boundaries
- Double-sided terrain rendering without an artificial skirt or bottom cap

### Changed

- Reworked texture loading as Texture Pipeline V2
- Updated the persistent PrefabTree cache schema
- Terrain cells are no longer treated as unsupported blocks
- Corrected terrain placement relative to regular blocks and the voxel grid
- Terrain is rendered with `cull_mode: None`, matching its visibility from below in 7 Days to Die
- Improved presentation controls for lighting and fog

### Fixed

- Fixed an old persistent PrefabTree cache preventing the new cache from being saved
- Fixed terrain density pairing after the Z-axis flip
- Fixed terrain triangle winding after coordinate conversion
- Fixed the terrain half-block placement offset
- Fixed vegetation transparency

### Performance

- Practically eliminated CPU decoding for commonly supported compressed textures
- Reduced texture-data RAM usage by up to approximately 80% in tested cases
- Improved subsequent POI loading through the corrected persistent PrefabTree cache

## [0.1.0-pre.1] - 2026-08-29

### Added

- First public experimental Windows release
- Standalone POI loading and interactive 3D viewing
- ShapeNew geometry and paint support
- ModelEntity loading
- Texture and material support
- Sign rendering
- Staged POI loader with progress reporting and POI preview
- Safe POI scene switching
- Persistent cache
- Runtime logging
- English user interface

[Unreleased]: https://github.com/xvgray/superdummy-releases/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/xvgray/superdummy-releases/releases/tag/v0.1.0
[0.1.0-pre.3]: https://github.com/xvgray/superdummy-releases/compare/v0.1.0-pre.2...v0.1.0-pre.3
[0.1.0-pre.2]: https://github.com/xvgray/superdummy-releases/compare/v0.1.0-pre.1...v0.1.0-pre.2
[0.1.0-pre.1]: https://github.com/xvgray/superdummy-releases/releases/tag/v0.1.0-pre.1
