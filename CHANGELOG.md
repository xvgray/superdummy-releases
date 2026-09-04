# Changelog

All notable changes to SuperDummy will be documented in this file.

SuperDummy is currently in an experimental pre-release stage. Features, file formats and behaviour may change between releases.

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

[0.1.0-pre.2]: https://github.com/xvgray/superdummy-releases/releases/tag/v0.1.0-pre.2
[0.1.0-pre.1]: https://github.com/xvgray/superdummy-releases/releases/tag/v0.1.0-pre.1
