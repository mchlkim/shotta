# Shotta User Guide

Shotta is a macOS menu bar screenshot tool. You can capture a full screen, region, or window, then edit the image or save it as a PNG file.

Choose [DMG or ZIP](../README.md#download-and-install). Both contain the same app. Install it in Applications before launching it.

## Image files and Save As

Use **File > Open Images…** (Command+O), the menu bar's Open Images command, Finder's **Open With > Shotta**, or drag files into the editor. Supported input formats are PNG, JPEG, WebP, HEIC/HEIF, TIFF, BMP and GIF. Multiple files join history in order; animated or multi-page files open only the first frame/page. Images over 64 million pixels or 256 MiB of decoded data are rejected. File opening does not require Screen Recording permission or trigger capture auto-save.

Use **File > Save As…** (Shift+Command+S), or right-click the editor's Save button, to choose a folder, filename and PNG/JPEG/TIFF/HEIC/BMP format. PNG and TIFF preserve transparency; JPEG, HEIC and BMP use a white background. WebP is supported for opening only. The system asks before replacing an existing file.

Command+S and the Save button's normal click still create a new PNG in the configured folder. Imports do not modify the source file. Save As replaces a source file only if you explicitly choose that file and confirm replacement.

## Getting Started

1. Launch `Shotta.app`.
2. Confirm that the Shotta icon appears on the right side of the macOS menu bar.
3. When macOS asks for Screen Recording permission during your first capture, allow it.

If macOS blocks the first launch with a warning that the app could not be verified, open `System Settings` > `Privacy & Security` and click `Open Anyway`. See the [README](../README.md) for details.

Shotta is a menu bar app. It does not open a large main window immediately after launch. Start captures from the menu bar or global shortcuts.

## Basic Capture

Click the Shotta icon in the menu bar to use these commands.

| Menu | Default Shortcut | Action |
| --- | --- | --- |
| Region Capture | `Control + Option + Shift + 4` | Capture a dragged rectangle. |
| Full Screen Capture | `Control + Option + Shift + 3` | Capture the display you click. |
| Window Capture | `Control + Option + Shift + 5` | Capture the highlighted window under the pointer. |

When the capture overlay is open:

| Key or Action | Description |
| --- | --- |
| `Space` | Switch modes in this order: full screen, region, window. |
| `Esc` | Cancel capture and close the overlay. |
| Drag | Select an area in region capture mode. |
| Click | Capture the current highlighted target in full screen or window mode. |

In multi-display setups, Shotta shows an overlay on every display. Full screen capture uses the display you click, and region capture can cross display boundaries.

The magnifier helps you check the edges while selecting a region. Adjust its size and zoom in Settings.

## Shortcut recording permission

When recording a new shortcut in Settings, Shotta may request Accessibility permission to receive the key combination before other apps. Allow it in `System Settings` > `Privacy & Security` > `Accessibility` if prompted. Input interception is active only while recording a shortcut. Opening image files does not require Screen Recording permission.

## After Capture

By default, Shotta opens the editor after a capture. In Settings, you can change the after-capture action to copy directly to the clipboard instead. In that mode, Shotta copies the capture and shows a short completion message.

Choose `Open Editor` from the menu bar menu to reopen the latest capture or the current editor.

## Editor

Use the toolbar to edit the image. You can place the toolbar on the left, top, or bottom in Settings.

| Tool | Description |
| --- | --- |
| Copy | Copy the current edited result to the clipboard. |
| Save | Save the current edited result as a PNG file. |
| Undo / Redo | Revert or reapply edits. |
| Select | Select, move, and resize existing annotations. |
| Rectangle / Ellipse / Arrow / Line | Draw shapes on the image. |
| Pen | Draw freehand lines. |
| Highlight | Add highlight marks. |
| Text | Add text on the image. |
| Crop | Keep only the selected area. |
| Blur | Apply blur or mosaic to a selected area. |

Depending on the selected tool or object, you can adjust color, stroke width, text size, effect type, and effect strength. Copy and save use the current visible edited result.

## Live Text

When the Select tool is active, Shotta recognizes text inside the current capture. Drag across text in the image to select it, then press `Command + C` to copy the selected text instead of the image. Press `Esc` or switch to another tool to clear the text selection.

Text recognition runs entirely on-device. If nothing is selectable, the capture may not contain recognizable text.

## Editor Shortcuts

| Shortcut | Action |
| --- | --- |
| `Command + C` | Copy edited result |
| `Command + O` | Open image files |
| `Shift + Command + S` | Save As: choose name, folder, and format |
| `Command + S` | Save edited result |
| `Command + Z` | Undo |
| `Command + Shift + Z` or `Command + Y` | Redo |
| `Command + +` | Zoom in |
| `Command + -` | Zoom out |
| `Space` | Return to fit-to-screen position |
| `Esc` | Cancel the current tool or selection action |
| `Return` | Confirm crop selection |
| `Delete` | Delete selected annotation |
| `Command + A` | Select all annotations |
| `Command + W` | Close editor window |
| `Command + ,` | Open Settings |

Tool shortcuts:

| Key | Tool |
| --- | --- |
| `R` | Rectangle |
| `O` | Ellipse |
| `A` | Arrow |
| `D` | Pen |
| `H` | Highlight |
| `T` | Text |
| `C` | Crop |
| `B` | Blur |

Adjustment shortcuts:

| Shortcut | Action |
| --- | --- |
| `Option + +` | Increase selected stroke width or blur strength |
| `Option + -` | Decrease selected stroke width or blur strength |

## History

The editor history panel keeps up to 100 captures and imported images together. Click a thumbnail to return to an image.

When the history panel is open:

| Action | Description |
| --- | --- |
| `Option + Up` | Move to a newer capture |
| `Option + Down` | Move to an older capture |
| `Option + Mouse Wheel` | Move through history items |
| Right-click thumbnail | Show copy, reveal saved file, and delete actions |

For history items with saved files, the right-click menu can reveal the saved location.

## Settings

Open Settings from the Shotta menu bar icon or with `Command + ,`.

### General

| Item | Description |
| --- | --- |
| Screenshot Folder | Default folder for saving and auto-save. |
| Auto Save | Automatically save a PNG for every capture. |
| Launch at Login | Start Shotta automatically when you sign in to macOS. |
| Language | Choose English, Korean, Chinese, or Japanese. |
| After Capture | Open the editor or copy directly to the clipboard. |
| Toolbar Position | Place the editor toolbar on the left, top, or bottom. |

Auto-save file names use the `shotta-YYYYMMDD-HHMM.png` format. If multiple files are created in the same minute, Shotta appends a number such as `shotta-YYYYMMDD-HHMM 2.png`.

### Shortcuts

Use the Shortcuts tab to change global shortcuts for full screen, region, and window capture. Click a shortcut field, enter a new key combination, and it is saved. Use the reset button to restore a default shortcut.

If another app or macOS already uses the same global shortcut, Shotta may not be able to register it. Choose a different shortcut if one does not respond.

## Troubleshooting

### Captures Are Black or Empty

Check Screen Recording permission in `System Settings` > `Privacy & Security` > `Screen Recording`, allow Shotta, then relaunch the app.

### Shortcuts Do Not Respond

Check the Shortcuts tab in Settings. Another app may already be using the same global shortcut.

### Shotta Keeps Asking for Permissions

Development builds or ad-hoc signed apps can look like different apps to macOS after each rebuild. Use the same bundle identifier and signing identity for fewer repeated permission prompts.

### Quit Shotta Completely

Click the Shotta icon in the menu bar, then choose `Quit`. Closing only the editor window leaves Shotta running in the menu bar.

## Uninstall

1. Click the Shotta icon in the menu bar and choose `Quit`.
2. Delete `Shotta.app` from your Applications folder.
3. Optionally remove settings: run `defaults delete com.local.Shotta` in Terminal.
4. Optionally remove Shotta from `System Settings` > `Privacy & Security` > `Screen Recording` and `Accessibility`.

Saved images remain in your chosen folder and format. Auto-saved captures are PNG files.
