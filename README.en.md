<div align="center">

<img src="assets/logo.svg" alt="DeskChatGPT" width="88">

# DeskChatGPT

Work with Mac files, run commands, and control your desktop from ChatGPT. You decide what it can access.

[![Latest release](https://img.shields.io/github/v/release/jiangxinlei/DeskChatGPT?style=flat-square&color=orange)](https://github.com/jiangxinlei/DeskChatGPT/releases/latest)
[![Total downloads](https://img.shields.io/github/downloads/jiangxinlei/DeskChatGPT/total?style=flat-square&logo=github&color=brightgreen)](https://github.com/jiangxinlei/DeskChatGPT/releases)

[Features](#features) · [Download](#download) · [Usage](#usage) · [Support](#support)

</div>

## Features

- **Files and projects:** Browse folders, search and read files, create, edit, move, delete, and perform batch changes with review and supported recovery.
- **Terminal and Git:** Run commands, builds, and tests; inspect task output and status; stop running tasks.
- **Isolated browser:** Open and inspect websites, interact with pages, fill forms, and capture screenshots.
- **Desktop control:** List and open apps, capture screens, and interact with windows using macOS permissions.
- **Flexible permissions:** Choose read-only, per-change approval, or direct read/write for folders. Grant Terminal, browser, and desktop access separately.
- **Multiple Macs:** Connect each Mac independently and choose which one to use in ChatGPT; files and permissions are not automatically shared.
- **Activity history:** Review task states, file changes, and execution receipts.

## Download

The macOS installers are available in the [v0.4.3 release](https://github.com/jiangxinlei/DeskChatGPT/releases/tag/v0.4.3) and require macOS 26 or later.

| Platform | Architecture          | Package | Progress                                                                 |
| -------- | --------------------- | ------- | ------------------------------------------------------------------------ |
| macOS    | Apple Silicon (arm64) | [DMG](https://github.com/jiangxinlei/DeskChatGPT/releases/download/v0.4.3/DeskChatGPT-0.4.3-macos-arm64.dmg) | Published. Startup and Tunnel connection verified on an Apple silicon Mac. |
| macOS    | Intel (x64)           | [DMG](https://github.com/jiangxinlei/DeskChatGPT/releases/download/v0.4.3/DeskChatGPT-0.4.3-macos-x64.dmg) | Published. Desktop regression passed under Rosetta. Testing on an Intel Mac is pending. |
| Windows  | x64                   | EXE     | Native implementation and installer in development; not downloadable yet |

## Usage

1. Create a private Tunnel on OpenAI Platform and connect this Mac in DeskChatGPT.
2. Add the corresponding custom MCP tool to your ChatGPT workspace.
3. Grant the folders you need in Workbench. Start with **read-only** access.
4. Select DeskChatGPT in ChatGPT and begin working with your files or projects. Use per-change approval for reviewed edits.

See [Getting started](docs/en/start.md) for step-by-step instructions.

## Documentation

[Getting started](docs/en/start.md) · [Permissions and security](docs/en/safety.md) · [Data and privacy](docs/en/privacy.md) · [FAQ](docs/en/faq.md)

> Terminal and Git run under your OS user. Tool results may return to ChatGPT. See [Security](SECURITY.md) for permission boundaries and limitations.

## Support

For bugs and feature requests, visit [GitHub Issues](https://github.com/jiangxinlei/DeskChatGPT/issues). If the project helps you, consider starring the repository.

---

<sub>DeskChatGPT is independently developed and is not affiliated with or endorsed by OpenAI.</sub>
