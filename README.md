<p align="center">
  <img src="assets/app-icon.png" alt="Shotta app icon" width="128" height="128">
</p>

<h1 align="center">Shotta</h1>

<p align="center">
  <strong>Capture. Mark it up. Send it.</strong><br>
  A Mac screenshot tool that keeps your workflow moving.
</p>

<p align="center">
  <a href="https://shotta-mac.mchlkim.chatgpt.site/en">Website</a> ·
  <a href="downloads/Shotta.app.zip">Download</a> ·
  <a href="docs/user-guide.en.md">User Guide</a> ·
  <a href="../../issues">Feedback</a>
</p>

<p align="center">
  <img alt="Platform" src="https://img.shields.io/badge/platform-macOS%2026%2B-blue">
  <img alt="Architecture" src="https://img.shields.io/badge/chip-Apple%20Silicon-lightgrey">
  <img alt="Version" src="https://img.shields.io/badge/version-1.1.0-brightgreen">
  <img alt="License" src="https://img.shields.io/badge/license-Freeware-orange">
</p>

Capture what you need, blur what you don't, and send it right away. Shotta lives in your Mac menu bar, ready whenever you need a clean screenshot without switching tools or uploading anything.

## Capture exactly what you need

Start from the menu bar or a keyboard shortcut. Use `Space` to switch capture modes, or press `Esc` whenever you want to cancel.

| Capture mode | What it does |
| --- | --- |
| Full screen | Captures an entire display, including multi-monitor setups. |
| Region | Lets you drag out exactly the area you need. |
| Window | Captures the window under your pointer with one click. |
| UI element | Captures a visible button, field, list, or other interface element. |

## Mark up and share

Once you've captured it, you're halfway done explaining. Add a note where it matters, hide sensitive information, copy text directly from the image, or reopen an earlier capture from your history.

- Shapes, arrows, lines, pen, highlighter, and text
- Crop, blur, and mosaic
- Live Text with on-device text recognition
- Copy to the clipboard, save quickly as PNG, or use **Save As…** (⇧⌘S) to choose a folder, filename and PNG/JPEG/TIFF/HEIC/BMP format
- Open PNG, JPEG, WebP, HEIC/HEIF, TIFF, BMP and GIF images with ⌘O, Finder or file drop
- Recent capture and imported-image history with compressed thumbnails and inactive originals

## New in v1.1.0

Image file opening and **Save As…** join the existing capture editor. Capture dimming uses compositing layers, overlay windows are reused, and image caches retain fewer inactive bitmaps. See the [changelog](CHANGELOG.md#110--2026-09-08) for details.

## Private by default

Your screenshots stay on your Mac. Capturing, editing, and text recognition all happen locally: no uploads, no tracking, and no sign-in.

## Requirements

- macOS 26 or later
- Apple Silicon Mac (the current build is arm64-only)

## Download and install

Download the latest app package: [Shotta.app.zip](downloads/Shotta.app.zip).

The stable raw download URL is:

```text
https://github.com/mchlkim/shotta/raw/main/downloads/Shotta.app.zip
```

Release metadata for app-driven update checks is available at [downloads/latest.json](downloads/latest.json). Version history is in the [changelog](CHANGELOG.md).

Unzip the archive and move `Shotta.app` to your Applications folder. Shotta runs from the macOS menu bar, so it does not open a large main window on startup.

### Verify the download (optional)

Compare the SHA-256 checksum of the downloaded archive with the value in [downloads/latest.json](downloads/latest.json):

```sh
shasum -a 256 Shotta.app.zip
```

## Frequently asked questions

<details>
<summary><strong>macOS says Shotta cannot be opened. What should I do?</strong></summary>

The current build is not notarized by Apple. Move `Shotta.app` to Applications, then Control-click it in Finder and choose **Open**. Choose **Open** again in the dialog. This is the usual one-time way to approve a downloaded app you trust.
</details>

<details>
<summary><strong>I cannot find the Open option in Finder.</strong></summary>

Try opening Shotta normally once. Then go to **System Settings → Privacy & Security**, scroll to **Security**, and choose **Open Anyway** next to the Shotta message. Confirm **Open** when macOS asks again.
</details>

<details>
<summary><strong>Why does macOS show this warning?</strong></summary>

This build has not been notarized by Apple, so Gatekeeper asks for your approval before the first launch. The warning is about the distribution status; you do not need to disable macOS security globally.
</details>

<details>
<summary><strong>Which permissions does Shotta need?</strong></summary>

Screen capture requires **Screen Recording** permission. UI element capture also uses **Accessibility** permission to detect the visible element under the pointer. Manage both in **System Settings → Privacy & Security**.
</details>

<details>
<summary><strong>What Mac do I need?</strong></summary>

Shotta requires macOS 26 or later on an Apple Silicon Mac. After the first-launch approval, it runs directly from the menu bar.
</details>

## Keyboard shortcuts

### Start a capture

These are the default global shortcuts. You can change them in Shotta Settings.

| Shortcut | Action |
| --- | --- |
| `Control + Option + Shift + 3` | Capture a full screen |
| `Control + Option + Shift + 4` | Capture a selected area |
| `Control + Option + Shift + 5` | Capture a window |
| `Control + Option + Shift + 6` | Capture a UI element |

### Edit faster

| Shortcut | Action |
| --- | --- |
| `R` · `O` · `A` · `L` | Rectangle · oval · arrow · line |
| `D` · `H` · `T` | Pen · highlighter · text |
| `C` · `B` | Crop · blur |
| `Command + C` · `Command + S` | Copy · save |
| `Command + Z` · `Command + Shift + Z` | Undo · redo |
| `Command + +` · `Command + -` · `Space` | Zoom in · zoom out · reset view |
| `Delete` · `Esc` · `Return` | Delete selection · cancel · apply crop |

## Guides in your language

English is the default language for this repository.

| Language | Product overview | User guide | Website |
| --- | --- | --- | --- |
| English | [Overview](docs/overview.en.md) | [User Guide](docs/user-guide.en.md) | [English](https://shotta-mac.mchlkim.chatgpt.site/en) |
| 한국어 | [제품 소개](docs/overview.ko.md) | [사용자 가이드](docs/user-guide.ko.md) | [한국어](https://shotta-mac.mchlkim.chatgpt.site/ko) |
| 简体中文 | [产品介绍](docs/overview.zh.md) | [用户指南](docs/user-guide.zh.md) | [简体中文](https://shotta-mac.mchlkim.chatgpt.site/zh) |
| 日本語 | [製品紹介](docs/overview.ja.md) | [ユーザーガイド](docs/user-guide.ja.md) | [日本語](https://shotta-mac.mchlkim.chatgpt.site/ja) |

## Permissions

Shotta may ask for macOS Screen Recording permission when you capture the screen. Element capture also uses Accessibility permission to detect the visible UI element under the pointer.

You can manage these permissions in macOS System Settings under Privacy & Security.

## Privacy

Shotta works entirely on your Mac.

- No network access: Shotta contains no networking code, so nothing is ever uploaded.
- No telemetry, analytics, or crash reporting.
- Captures exist only where you put them: the clipboard, the editor, and the save folder you choose.
- Text recognition (Live Text) runs on-device using macOS system frameworks.

## Uninstall

1. Click the Shotta icon in the menu bar and choose `Quit`.
2. Delete `Shotta.app` from your Applications folder.
3. Optionally remove settings: run `defaults delete com.local.Shotta` in Terminal.
4. Optionally remove Shotta from `System Settings` > `Privacy & Security` > `Screen Recording` and `Accessibility`.

Screenshots you saved or auto-saved are regular PNG files and remain in your chosen folder.

## Feedback

Bug reports and feature requests are welcome in [GitHub Issues](../../issues). Please include your macOS version and, for capture problems, whether Screen Recording permission is granted.

## License

Shotta is free to use for personal and commercial purposes. See [LICENSE](LICENSE) for the full terms. No warranty is provided.

## Source Code

This repository is for public distribution, product information, user guides, and release artifacts. The source code is maintained separately.
