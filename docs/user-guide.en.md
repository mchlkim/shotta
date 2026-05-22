# Shotta User Guide

Shotta is a macOS menu bar screenshot tool. You can capture a full screen, region, window, or visible UI element, then edit the image or save it as a PNG file.

## Getting Started

1. Launch `Shotta.app`.
2. Confirm that the Shotta icon appears on the right side of the macOS menu bar.
3. When macOS asks for Screen Recording permission during your first capture, allow it.
4. If Element Capture asks for Accessibility permission, choose `Open System Settings` and allow Shotta.

Shotta is a menu bar app. It does not open a large main window immediately after launch. Start captures from the menu bar or global shortcuts.

## Basic Capture

Click the Shotta icon in the menu bar to use these commands.

| Menu | Default Shortcut | Action |
| --- | --- | --- |
| Region Capture | `Control + Option + Shift + 4` | Capture a dragged rectangle. |
| Full Screen Capture | `Control + Option + Shift + 3` | Capture the display you click. |
| Window Capture | `Control + Option + Shift + 5` | Capture the highlighted window under the pointer. |
| Element Capture | `Control + Option + Shift + 6` | Capture the highlighted UI element under the pointer. |

When the capture overlay is open:

| Key or Action | Description |
| --- | --- |
| `Space` | Switch modes in this order: full screen, region, window, element. |
| `Esc` | Cancel capture and close the overlay. |
| Drag | Select an area in region capture mode. |
| Click | Capture the current highlighted target in full screen, window, or element mode. |

In multi-display setups, Shotta shows an overlay on every display. Full screen capture uses the display you click, and region capture can cross display boundaries.

## Element Capture Permission

Element Capture uses macOS Accessibility permission to detect UI elements such as buttons, input fields, and list rows under the pointer.

If permission is missing, Shotta shows a permission prompt. Choose `Open System Settings`, then allow Shotta under `Privacy & Security` > `Accessibility`. If elements still do not highlight after permission is granted, quit and relaunch Shotta.

Element Capture captures the visible area of the detected accessibility element. It does not capture an entire webpage or hidden DOM content outside the visible screen.

## After Capture

By default, Shotta opens the editor after a capture. In Settings, you can change the after-capture action to copy directly to the clipboard instead. In that mode, Shotta copies the capture and shows a short completion message.

Choose `Open Editor` from the menu bar menu to reopen the latest capture or the current editor.

## Editor

Use the left or top toolbar to edit the image. You can change the toolbar position in Settings.

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

## Editor Shortcuts

| Shortcut | Action |
| --- | --- |
| `Command + C` | Copy edited result |
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

The editor history panel keeps up to 100 recent captures. Click a thumbnail to switch to another capture.

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
| Toolbar Position | Place the editor toolbar on the left or at the top. |

Auto-save file names use the `shotta-YYYYMMDD-HHMM.png` format. If multiple files are created in the same minute, Shotta appends a number such as `shotta-YYYYMMDD-HHMM 2.png`.

### Shortcuts

Use the Shortcuts tab to change global shortcuts for full screen, region, window, and element capture. Click a shortcut field, enter a new key combination, and it is saved. Use the reset button to restore a default shortcut.

If another app or macOS already uses the same global shortcut, Shotta may not be able to register it. Choose a different shortcut if one does not respond.

## Troubleshooting

### Captures Are Black or Empty

Check Screen Recording permission in `System Settings` > `Privacy & Security` > `Screen Recording`, allow Shotta, then relaunch the app.

### Element Capture Does Not Select Anything

Check Accessibility permission. Some apps limit accessibility information, and secure input areas such as password fields may not be available for element capture.

### Shortcuts Do Not Respond

Check the Shortcuts tab in Settings. Another app may already be using the same global shortcut.

### Shotta Keeps Asking for Permissions

Development builds or ad-hoc signed apps can look like different apps to macOS after each rebuild. Use the same bundle identifier and signing identity for fewer repeated permission prompts.

### Quit Shotta Completely

Click the Shotta icon in the menu bar, then choose `Quit`. Closing only the editor window leaves Shotta running in the menu bar.
