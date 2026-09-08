# Changelog

All notable changes to Shotta releases are documented here. The latest release
metadata is also published in [downloads/latest.json](downloads/latest.json).

## [1.1.0] — 2026-09-08

### Added

- Open PNG, JPEG, WebP, HEIC/HEIF, TIFF, BMP and GIF images with Command+O, Finder's Open With, or file drop. Animated and multi-page files open their first frame/page.
- Save As (Shift+Command+S) lets you choose the folder, filename and PNG/JPEG/TIFF/HEIC/BMP format. PNG/TIFF preserve transparency; JPEG/HEIC/BMP use a white background. Existing Command+S remains quick PNG save.
- Imported files join capture history without triggering capture auto-save or modifying their source files.

### Improved

- Composite capture dimming with CALayer instead of CPU full-screen fills.
- Reuse capture overlay windows, preparing new pixels before presentation and releasing old snapshots afterwards.
- Store history thumbnails as compressed PNG data and compress inactive originals losslessly.
- Manage retained effect pixels with a 128 MiB target; active effects may exceed the target to avoid repeated recomputation.

### Validation and distribution

- 381 automated tests passed; Release build and local signature verification passed.
- Native GUI interaction testing and updated end-to-end capture timing have not been completed.
- macOS 26+, Apple Silicon. This build uses a local development signature and is not notarized by Apple.

## [1.0.0]

Initial public release.

### Capture

- Full screen, region, window, and visible UI element capture
- Capture overlay across all displays, with region selections that can cross display boundaries
- Frozen-screen overlay: the final image matches the moment the overlay opened
- Global shortcuts for every capture mode, configurable in Settings

### Editor

- Annotation tools: rectangle, ellipse, arrow, line, freehand pen, highlighter, text
- Crop, blur, and mosaic for hiding sensitive content
- Live Text: select and copy text recognized inside the capture
- Per-capture undo and redo
- Capture history with up to 100 recent captures
- Zoom in, zoom out, and fit to screen
- Copy to clipboard or save as PNG, with optional auto-save

### App

- Menu bar app with no dock icon
- Light, dark, and system appearance
- UI languages: English, Korean, Chinese, and Japanese
- Launch at login option
