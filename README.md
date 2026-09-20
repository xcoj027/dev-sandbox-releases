<div align="center">

<img src="https://happy-number.cloud/favicon/apple-touch-icon.png" alt="Dev Sandbox Logo" width="128" height="128">

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
  - **Gradle Projects**: Automatically detects Spring Boot modules (`bootRun`) and Gradle application plugins (`run`).
  - **Maven Projects**: Recursively parses `pom.xml` modules to identify Spring Boot Maven and Exec Maven applications.
  - **Web Frontends**: Detects Node/React/Vue/Angular apps from `package.json`, automatically determining the correct package manager (`npm`, `pnpm`, `yarn`, `bun`).
- **Port Conflict Adoption**:
  - If a service port is already in use by a zombie or background process from a previous session, Dev Sandbox safely adopts that PID instead of failing on startup.
- **Interactive Multi-Service Console**:
  - Real-time log streaming with ANSI colorization.
  - Filter logs by level: `INFO`, `WARN`, `ERROR`, `DEBUG`, `SYSTEM`.
  - Search with real-time match highlighting and navigation (`Previous` / `Next`).
  - Selection-aware log copying and full file export.
- **Tree-Process Termination**:
  - Gracefully stops processes and all their child processes (`ProcessHandle.descendants()`) to prevent rogue background worker leaks.
  - Safely verifies all processes exit before closing or switching project roots.
- **Environment & Port Customization**:
  - Override ports or inject custom environment variables per service directly through the UI.

---

## Installation & Quick Start

### macOS
1. Download `DevSandbox-macos.dmg`.
2. Double-click the `.dmg` file and drag **Dev Sandbox** into your `/Applications` folder.
3. Launch **Dev Sandbox** from Spotlight or Applications.
4. Select your project root folder (containing `settings.gradle` or `pom.xml`).

### Windows
1. Download `DevSandbox-windows-x64.zip`.
2. Extract the ZIP archive anywhere on your system.
3. Double-click `DevSandbox.exe` to run.
4. Select your workspace root folder.

### Linux
- **Debian / Ubuntu**:
  ```bash
  sudo dpkg -i dev-sandbox-linux.deb
  ```
  Launch from your application menu or terminal via `dev-sandbox`.
- **Portable Tarball**:
  ```bash
  tar -xvf DevSandbox-linux-x64.tar.gz
  ./DevSandbox/bin/DevSandbox
  ```

### Universal JAR (Any OS with Java 21+)
```bash
java -jar dev-sandbox-universal.jar
# or run headless CLI scan mode:
java -jar dev-sandbox-universal.jar --scan /path/to/project
```

---

## Verification & Integrity

Every release includes a `SHA256SUMS.txt` file containing cryptographic hashes for all published artifacts.

To verify a downloaded file:
```bash
# macOS / Linux
sha256sum -c SHA256SUMS.txt

# Windows (PowerShell)
Get-FileHash DevSandbox-windows-x64.zip -Algorithm SHA256
```

---

## Author & Brand

Designed and maintained by **TNQ MEDIA**  
GitHub: [@xcoj027](https://github.com/xcoj027)

For issue reports, feature suggestions, or questions, please open an [Issue](https://github.com/xcoj027/dev-sandbox-release/issues).

---

## License

This software is distributed under the [MIT License](LICENSE).
