<p align="center">
  <img src="assets/app-icon.png" alt="Shotta app icon" width="128" height="128">
</p>

<h1 align="center">Shotta</h1>

<p align="center">
  <strong>One image. Point made.</strong><br>
  Capture your screen. Or start with an image you already have.
</p>

<p align="center">
  <a href="https://shotta.mchlkim.com/en">Website</a> ·
  <a href="https://github.com/mchlkim/shotta/releases/latest/download/Shotta.dmg">Download DMG</a> ·
  <a href="https://github.com/mchlkim/shotta/releases/latest/download/Shotta.app.zip">ZIP</a> ·
  <a href="docs/user-guide.en.md">User guide</a> ·
  <a href="CHANGELOG.md">Changelog</a> ·
  <a href="../../issues">Feedback</a>
</p>

<p align="center">
  <img alt="Platform" src="https://img.shields.io/badge/platform-macOS%2026%2B-blue">
  <img alt="Architecture" src="https://img.shields.io/badge/chip-Apple%20Silicon-lightgrey">
  <img alt="Version" src="https://img.shields.io/badge/version-1.2.3-brightgreen">
  <img alt="License" src="https://img.shields.io/badge/license-Freeware-orange">
</p>

Shotta lives in your Mac menu bar. Capture a screen or open an image, add a note, and blur sensitive details before you copy or save. Editing and text recognition happen on your Mac.

## New in v1.2.3

- Fix the screenshot-folder control's layout and opaque background in Settings.
- Align the Update label and status text in Settings > About.
- Refresh the Shotta menu when the app becomes active, and add **Check for Updates…** to both the app menu and the menu bar status icon.

See the [v1.2.3 changelog](CHANGELOG.md#123--2026-09-12) for details.

## New in v1.2.2

- **Install updates in the app.** Open Settings > About, check for an update, then choose **Install Update…**. Sparkle verifies the download, replaces the app, and handles relaunching after you approve installation.
- **Signed update archives.** Ed25519 signatures are checked before extraction. Automatic version checks do not automatically install updates.
- **One-time migration.** If you use 1.2.1 or earlier, manually install 1.2.2 once to enable in-app installation for future releases.

See the [v1.2.2 changelog](CHANGELOG.md#122--2026-09-12) for details.

## New in v1.2.0

- **See the size while you select.** While dragging a region, a label shows the output size in pixels (for example `1280 × 720 px`) and the top-left position of the selection on the display where the drag started.
- **Nudge to the exact pixel.** Hold the mouse button and press an arrow key to move the selection's end point by 1 pt, or 10 pt with `Shift`. The magnifier follows, and releasing the mouse still captures immediately.
- **Open the editor from anywhere.** `Control + Option + Shift + E` brings up the editor with your latest capture. Change it in Settings > Shortcuts.
- **Downloads live on GitHub Releases.** The DMG and ZIP links below always point to the newest release.

See the [v1.2.0 changelog](CHANGELOG.md#120--2026-09-10) for details.

## Fixed in v1.1.2

- Fix a crash caused by repeated Live Text selection callbacks while moving images or annotations.
- Keep programmatic OCR updates separate from user selection and preserve OCR selection when the same image is refreshed.
- Clear OCR results when their image is removed from history.
- Keep copy and undo/redo shortcuts inside the active text editor.

See the [v1.1.2 changelog](CHANGELOG.md#112--2026-09-09) for details.

## Added in v1.1.0

- **Open images.** Use `Command + O`, Finder's **Open With**, or a file drop. Imported images join your capture history.
- **Choose how to save.** Use `Shift + Command + S` to choose the name, folder, and image format. `Command + S` still saves a new PNG in your configured folder.
- **Three capture modes.** Full screen, region, and window. UI element capture and its `Control + Option + Shift + 6` shortcut have been removed.
- **Less memory held between edits.** History images are compressed when inactive, and capture overlay windows are reused.

See the [v1.1.0 changelog](CHANGELOG.md#110--2026-09-08) for the full changes and validation notes.

## Capture just what you need

Start from the menu bar or a shortcut. Press `Space` to cycle through full screen, region, and window capture. Use the magnifier to check the edges of your selection, or press `Esc` to cancel.

| Capture mode | What it does |
| --- | --- |
| Full screen | Captures the display you click, including in a multi-monitor setup. |
| Region | Captures the area you drag, even across display boundaries. |
| Window | Captures the highlighted window under your pointer. |

## A few marks. A clearer message.

Point with an arrow, highlight a passage, or add a note. Blur or pixelate sensitive details before sharing the result.

- Shapes, arrows, lines, pen, highlighter, and text
- Crop, blur, and mosaic
- Live Text: select words in an image and copy them as text
- Undo and redo
- Copy the edited image or save a new file
- A shared history for recent captures and imported images

### Already have the image?

Open it with `Command + O`, drop it into the editor, or choose Shotta in Finder's **Open With** menu. Use the same editing tools you use for screenshots.

Shotta opens **PNG, JPEG, WebP, HEIC/HEIF, TIFF, BMP, and GIF**. Animated and multipage images open at the first frame or page. Importing does not change the original file or trigger capture auto-save.

### Save it your way

| Action | Result |
| --- | --- |
| `Command + S` | Saves a new PNG in your configured folder. |
| `Shift + Command + S` | Opens **Save As…** to choose the name, folder, and format. |
| Right-click the Save button | Opens the menu containing **Save As…**. |

Save As supports **PNG, JPEG, TIFF, HEIC, and BMP**. PNG and TIFF keep transparency; the other formats replace transparent areas with white. WebP is supported for opening only. If you choose an existing file, macOS asks before replacing it.

## Download and install

Shotta requires **macOS 26 or later on an Apple Silicon Mac**. The current download is **v1.2.2 (build 115)**, published on the [Releases page](https://github.com/mchlkim/shotta/releases).

| Format | Download | Installation |
| --- | --- | --- |
| DMG (recommended) | [Shotta.dmg](https://github.com/mchlkim/shotta/releases/latest/download/Shotta.dmg) | Open the disk image and drag Shotta to Applications. |
| ZIP | [Shotta.app.zip](https://github.com/mchlkim/shotta/releases/latest/download/Shotta.app.zip) | Unzip the archive and move Shotta.app to Applications. |

Both downloads contain the same v1.2.2 app. For the initial installation or an upgrade from 1.2.1 or earlier, quit Shotta before replacing it. Launch the copy in Applications, then eject the DMG if you used it. Shotta appears in the menu bar. Starting with 1.2.2, use Settings > About > Install Update… for future updates. Save unfinished edits before installing an update.

The app retains its development signature and is not notarized by Apple. Either format may show the first-launch warning described below.

Stable download links that always resolve to the newest release: [DMG](https://github.com/mchlkim/shotta/releases/latest/download/Shotta.dmg) · [ZIP](https://github.com/mchlkim/shotta/releases/latest/download/Shotta.app.zip). Older versions are available on the [Releases page](https://github.com/mchlkim/shotta/releases).

### Verify a download

[downloads/latest.json](downloads/latest.json) lists the version, the release tag, each asset's download URL, and each file's size and SHA-256 checksum. Run the command for the format you downloaded:

| Format | Command | Checksum in latest.json |
| --- | --- | --- |
| DMG | `shasum -a 256 Shotta.dmg` | `artifacts.dmg.sha256` |
| ZIP | `shasum -a 256 Shotta.app.zip` | `artifacts.zip.sha256` |

The original top-level ZIP fields remain available for existing download tools.

## Frequently asked questions

<details>
<summary><strong>macOS warns me when I open Shotta. What should I do?</strong></summary>

The current build is not notarized by Apple. Confirm that your copy came from the official Shotta download and [verify its checksum](#download-and-install). If macOS cannot verify the developer, try opening Shotta once. Then run this in Terminal to open System Settings:

```sh
open -a "System Settings"
```

1. Choose **Privacy & Security** and scroll to **Security**.
2. Choose **Open Anyway** beside the Shotta message, then confirm **Open**.

This command only opens Settings; you approve Shotta in the macOS dialog. If macOS says the app is damaged or will harm your Mac, do not open it. Download a fresh copy from the official source. See [Apple's first-launch guidance](https://support.apple.com/en-us/102445).

</details>

<details>
<summary><strong>Can I allow the first launch from Terminal?</strong></summary>

For a copy downloaded from this site or the official GitHub repository, [verify its checksum](#verify-a-download) and move `Shotta.app` to `/Applications` first. If the unnotarized-app warning blocks it, run:

```sh
/usr/bin/xattr -dr com.apple.quarantine "/Applications/Shotta.app"
```

This removes the download quarantine attribute from Shotta only. It preserves the app's signature and does not add Apple notarization. Open Shotta from Applications afterwards; Screen Recording permission is still required for capture.

If Terminal reports a permission error, use **Open Anyway** in **Privacy & Security**. A managed Mac may prevent launch under your organization's policy.

</details>

<details>
<summary><strong>Which permissions does Shotta need?</strong></summary>

Capturing your screen requires **Screen Recording** permission in **System Settings → Privacy & Security**. Opening and editing image files does not require it.

When you record a new shortcut in Settings, Shotta may request **Accessibility** permission so it can receive the key combination before other apps. That input interception is active only while recording a shortcut. It is not used to detect screen elements.
</details>

<details>
<summary><strong>Where did UI element capture go?</strong></summary>

UI element capture was removed in v1.1.0, along with its menu item and default `Control + Option + Shift + 6` shortcut. Use region capture for a specific part of an interface, or window capture for a whole window.
</details>

<details>
<summary><strong>Can I save as WebP?</strong></summary>

WebP is supported for opening only. Choose PNG, JPEG, TIFF, HEIC, or BMP in **Save As…**.
</details>

## Keyboard shortcuts

### Start a capture

These global shortcuts work while you use other apps. Change them in Shotta Settings.

| Shortcut | Action |
| --- | --- |
| `Control + Option + Shift + 3` | Capture a full screen |
| `Control + Option + Shift + 4` | Capture a selected area |
| `Control + Option + Shift + 5` | Capture a window |
| `Control + Option + Shift + E` | Open the editor |

### Open, edit, and save

| Shortcut | Action |
| --- | --- |
| `Command + O` | Open image files |
| `Shift + Command + S` | Save As: choose name, folder, and format |
| `R` · `O` · `A` · `L` | Rectangle · oval · arrow · line |
| `D` · `H` · `T` | Pen · highlighter · text |
| `C` · `B` | Crop · blur |
| `Command + C` · `Command + S` | Copy · quick PNG save |
| `Command + Z` · `Command + Shift + Z` | Undo · redo |
| `Command + +` · `Command + -` · `Space` | Zoom in · zoom out · reset view |
| `Delete` · `Esc` · `Return` | Delete selection · cancel · apply crop |

## Guides in your language

| Language | Product overview | User guide | Website |
| --- | --- | --- | --- |
| English | [Overview](docs/overview.en.md) | [User guide](docs/user-guide.en.md) | [English](https://shotta.mchlkim.com/en) |
| 한국어 | [제품 소개](docs/overview.ko.md) | [사용자 가이드](docs/user-guide.ko.md) | [한국어](https://shotta.mchlkim.com/ko) |
| 简体中文 | [产品介绍](docs/overview.zh.md) | [用户指南](docs/user-guide.zh.md) | [简体中文](https://shotta.mchlkim.com/zh) |
| 日本語 | [製品紹介](docs/overview.ja.md) | [ユーザーガイド](docs/user-guide.ja.md) | [日本語](https://shotta.mchlkim.com/ja) |

## Privacy

Shotta processes captures and imported images locally. It does not upload your images, collect usage analytics, or send crash reports. You do not need an account. Live Text uses macOS system frameworks to recognize text on your Mac.

## Uninstall

1. Choose **Quit** from the Shotta menu bar icon.
2. Delete `Shotta.app` from Applications.
3. To remove settings, run `defaults delete com.local.Shotta` in Terminal.
4. Optionally remove Shotta from **System Settings → Privacy & Security → Screen Recording** and **Accessibility**, if listed.

Images you saved remain in the folder you chose, in the format you selected. Auto-saved captures are PNG files.

## Feedback

Report bugs or suggest features in [GitHub Issues](../../issues). Include your macOS version and, for capture problems, whether Screen Recording permission is granted.

## License and source code

Shotta is free for personal and commercial use. See [LICENSE](LICENSE) for the full terms. No warranty is provided.

This repository contains product information, user guides, and release downloads. The source code is maintained separately.
