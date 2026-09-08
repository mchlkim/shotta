# Changelog

All notable changes to Shotta releases are documented here. The latest release
metadata is also published in [downloads/latest.json](downloads/latest.json).

## [1.1.1] — 2026-09-08

### Fixed

- Keep Live Text selection separate from annotation drawing, dragging, and resize handles. Cancel stale text-recognition callbacks when switching images.
- Stop copy, save, and crop when effect rendering fails instead of exporting an unprocessed image.
- Clear stale redo steps after a new edit and cancel active drags when switching documents.
- Preserve cached images and zoom when reselecting the current history item, while clearing text selection before copying that image.
- Load translations and cursor resources from the app bundle without requiring the development checkout.

### Improved

- Limit concurrent history compression and effect processing. Release queued images that are deleted or no longer needed and combine superseded effect requests.
- Validate required resources and read release metadata from the packaged app when preparing downloads.

### Validation and distribution

- DMG and ZIP downloads contain the same v1.1.1 app. The DMG includes an Applications shortcut; the existing ZIP link remains available. Both formats retain the app's development signature and require the same first-launch approval when prompted.

- 418 automated tests passed for this release; Release build and local signature verification passed.
- macOS 26+, Apple Silicon. This build uses a local development signature and is not notarized by Apple.
- Native end-to-end capture and VisionKit interactions have not been manually verified for this release.

## [1.1.0] — 2026-09-08

### Added

- Open PNG, JPEG, WebP, HEIC/HEIF, TIFF, BMP and GIF images with Command+O, Finder's Open With, or file drop. Animated and multi-page files open their first frame/page.
- Save As (Shift+Command+S) lets you choose the folder, filename and PNG/JPEG/TIFF/HEIC/BMP format. PNG/TIFF preserve transparency; JPEG/HEIC/BMP use a white background. Existing Command+S remains quick PNG save.
- Imported files join capture history without triggering capture auto-save or modifying their source files.

### Removed

- UI element capture, its menu item, and the default Control+Option+Shift+6 shortcut. Capture now offers full screen, region, and window modes; Space cycles through those three modes.
- Accessibility-based element detection and its permission prompts. Accessibility permission may still be requested when recording a new shortcut in Settings; keyboard interception runs only during shortcut recording.

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
