<div align="center">
<img src="assets/icon.png" alt="Dev Sandbox Logo" width="128" height="128">
# Dev Sandbox
### Lightweight Desktop Control Center & Microservices Launcher
**Automated workspace discovery, port conflict adoption, and real-time process supervision.**
[![Release](https://img.shields.io/github/v/release/xcoj027/dev-sandbox-release?include_prereleases&style=for-the-badge&logo=github&color=blue)](https://github.com/xcoj027/dev-sandbox-release/releases)
[![Platform](https://img.shields.io/badge/Platform-macOS%20%7C%20Windows%20%7C%20Linux-brightgreen?style=for-the-badge)](https://github.com/xcoj027/dev-sandbox-release/releases)
[![License](https://img.shields.io/badge/License-MIT-orange?style=for-the-badge)](https://github.com/xcoj027/dev-sandbox-release/blob/main/LICENSE)
[**Download Latest Release**](https://github.com/xcoj027/dev-sandbox-release/releases/latest) • [**Features**](#features) • [**Installation**](#installation--quick-start) • [**Documentation**](#how-it-works)
</div>
---
## What is Dev Sandbox?
Running multiple microservices, backend workers, and web frontend apps locally usually means juggling dozens of open terminal tabs, manually killing orphaned process IDs (PIDs), and deciphering interleaved console output.
**Dev Sandbox** is a standalone, cross-platform desktop control center that automatically inspects any Gradle, Maven, or web workspace, detects every runnable application, and provides a unified graphical dashboard to start, stop, restart, configure, and monitor your entire development stack with a single click.
---
## Downloads
Official standalone builds with an embedded Java runtime are available directly on the [**Releases Page**](https://github.com/xcoj027/dev-sandbox-release/releases/latest):
| Operating System | Package Format | Details | Download Link |
| :--- | :--- | :--- | :--- |
| **macOS** (Intel / Apple Silicon) | **`.dmg`** | Native installer with drag-and-drop to Applications | [Download `.dmg`](https://github.com/xcoj027/dev-sandbox-release/releases/latest) |
| **macOS** (Portable) | **`.zip`** | Portable `DevSandbox.app` bundle | [Download `.zip`](https://github.com/xcoj027/dev-sandbox-release/releases/latest) |
| **Windows** (64-bit) | **`.zip`** | Portable folder with `DevSandbox.exe` (no installation required) | [Download `.zip`](https://github.com/xcoj027/dev-sandbox-release/releases/latest) |
| **Linux** (Debian / Ubuntu) | **`.deb`** | Standard desktop package installer with launcher shortcut | [Download `.deb`](https://github.com/xcoj027/dev-sandbox-release/releases/latest) |
| **Linux** (Any Distro) | **`.tar.gz`** | Portable standalone binary bundle with embedded JRE | [Download `.tar.gz`](https://github.com/xcoj027/dev-sandbox-release/releases/latest) |
| **Universal (Cross-Platform)** | **`.jar`** | Pure executable JAR (requires Java 21+) | [Download `.jar`](https://github.com/xcoj027/dev-sandbox-release/releases/latest) |
> [!TIP]
> **No Java pre-installation required!** Native packages (`.dmg`, `.zip` for Windows, `.deb`, `.tar.gz`) come pre-bundled with a dedicated runtime image.
---
## Features
- **Zero-Configuration Discovery**: