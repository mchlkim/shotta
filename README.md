<p align="center">
  <img src="assets/app-icon.png" alt="Shotta app icon" width="128" height="128">
</p>

# Shotta

<p align="center">
  <img alt="Platform" src="https://img.shields.io/badge/platform-macOS%2026%2B-blue">
  <img alt="Architecture" src="https://img.shields.io/badge/chip-Apple%20Silicon-lightgrey">
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-brightgreen">
  <img alt="License" src="https://img.shields.io/badge/license-Freeware-orange">
</p>

Shotta is a macOS menu bar screenshot tool for capturing, editing, and sharing screenshots without breaking your flow.

Start a capture from the menu bar or a global shortcut, select a full screen, region, window, or visible UI element, then copy or save the result from the built-in editor.

<!--
TODO: Add real captures to assets/ and uncomment.
Suggested shots: capture overlay with element highlight, editor with annotations, history panel.

<p align="center">
  <img src="assets/screenshot-overlay.png" alt="Capture overlay" width="720">
  <img src="assets/screenshot-editor.png" alt="Editor with annotations" width="720">
</p>
-->

## Requirements

- macOS 26 or later
- Apple Silicon Mac (the current build is arm64-only)

## Download

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

## First Launch

The current builds are not notarized by Apple, so macOS Gatekeeper blocks the first launch with a warning that the app could not be verified.

To open Shotta anyway:

1. Try to open `Shotta.app` once and dismiss the warning.
2. Open `System Settings` > `Privacy & Security`, scroll down to the security section, and click `Open Anyway` next to the Shotta message.
3. Confirm the prompt. This is only needed once per downloaded build.

## Highlights

- Full screen, region, window, and visible UI element capture
- Multi-display capture overlay
- Built-in editor with shapes, arrows, freehand drawing, highlights, text, crop, blur, and mosaic
- Live Text: select and copy text inside a capture
- Copy to clipboard or save as PNG
- Recent capture history in the editor
- Configurable global shortcuts
- Optional auto-save and launch at login
- UI languages: English, Korean, Chinese, and Japanese

## Guides

English is the default language for this repository.

| Language | Product Intro | User Guide |
| --- | --- | --- |
| English | [Overview](docs/overview.en.md) | [User Guide](docs/user-guide.en.md) |
| Korean | [제품 소개](docs/overview.ko.md) | [사용자 가이드](docs/user-guide.ko.md) |
| Chinese | [产品介绍](docs/overview.zh.md) | [用户指南](docs/user-guide.zh.md) |
| Japanese | [製品紹介](docs/overview.ja.md) | [ユーザーガイド](docs/user-guide.ja.md) |

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
