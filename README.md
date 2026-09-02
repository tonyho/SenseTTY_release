# SenseTTY Releases

**Modern, All-in-One Cross-Platform Operations Console & AI Terminal for Developers & Engineers**

[![Platforms](https://img.shields.io/badge/Platforms-Linux%20%7C%20Windows%20%7C%20macOS%20%7C%20Android-green)]()
[![Release](https://img.shields.io/badge/Release-v1.0.2-blue)]()
[![License](https://img.shields.io/badge/License-MIT-orange)]()

[English](README.md) | [简体中文](README_zh.md)

![SenseTTY Workspace Overview](docs/OverView.png)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Downloads & Installation](#downloads--installation)
  - [macOS Installation & Gatekeeper Note](#macos-installation--gatekeeper-note)
  - [Linux AppImage](#linux-appimage)
  - [Android APK](#android-apk)
  - [Windows Portable](#windows-portable)
- [Key Features](#key-features)
  - [🖥️ Multi-Protocol Terminal & Connectivity](#️-multi-protocol-terminal--connectivity)
  - [🤖 AI Agent & Copilot](#-ai-agent--copilot)
  - [📱 Seamless Mobile & Desktop Experience](#-seamless-mobile--desktop-experience)
  - [📁 Dual-Pane SFTP & File Manager](#-dual-pane-sftp--file-manager)
  - [🔌 Built-in MCP (Model Context Protocol) Server](#-built-in-mcp-model-context-protocol-server)
  - [🎛️ Real-Time Server Monitoring](#️-real-time-server-monitoring)
  - [⚙️ Session Management & Workspace Sync](#️-session-management--workspace-sync)
- [Screenshots & Showcase](#screenshots--showcase)
- [Keyboard Shortcuts](#keyboard-shortcuts)
- [Bug Reports & Feedback](#bug-reports--feedback)
- [License](#license)

---

## Overview

**SenseTTY** is a next-generation, cross-platform operations workstation designed for developers, DevOps engineers, embedded developers, and system administrators. SenseTTY seamlessly bridges desktop operating systems (**Linux**, **Windows**, **macOS**) and mobile devices (**Android**) with unified configurations, terminal sessions, and cloud-ready intelligence.

Whether diagnosing remote Linux cloud servers over **SSH**, debugging industrial hardware over **Serial / RS-485 / Modbus**, transferring assets via **SFTP**, or leveraging **AI Copilot** to analyze terminal errors and execute generated commands, SenseTTY delivers a smooth, native, and high-performance workflow.

---

## Downloads & Installation

You can download the latest pre-compiled binaries from our [GitHub Releases](https://github.com/tonyho/SenseTTY_release/releases) or the official mirror:

| Platform | Architecture | Package | Download |
|:---------|:-------------|:--------|:---------|
| **macOS** | **Universal Binary** (Apple Silicon M1/M2/M3/M4 & Intel x86_64) | `.zip` (App Bundle) | [Download macOS](https://github.com/tonyho/SenseTTY_release/releases/latest) |
| **Linux** | x86_64 | `.AppImage` | [Download Linux AppImage](https://github.com/tonyho/SenseTTY_release/releases/latest) |
| **Android** | arm64-v8a, armeabi-v7a, x86_64 | `.apk` | [Download Android APK](https://github.com/tonyho/SenseTTY_release/releases/latest) |
| **Windows** | x64 | `.zip` (Portable) | [Download Windows ZIP](https://github.com/tonyho/SenseTTY_release/releases/latest) |

### macOS Installation & Gatekeeper Note

Since SenseTTY binaries are not yet notarized with an Apple Developer certificate, macOS Gatekeeper may display a warning upon launch: *"sensetty.app is damaged and cannot be opened"* or *"developer cannot be verified"*.

To allow execution:
1. Extract `sensetty-macos-*.zip` and drag `sensetty.app` to your `/Applications` folder (or keep in Downloads).
2. Open **Terminal** and run:
   ```bash
   # If placed in Applications:
   xattr -cr /Applications/sensetty.app

   # Or if running directly in Downloads:
   xattr -cr ~/Downloads/sensetty.app
   ```
3. Launch SenseTTY directly from Finder or Launchpad.

### Linux AppImage
1. Download `sensetty-linux-x64-*.AppImage`.
2. Grant executable permission:
   ```bash
   chmod +x sensetty-linux-x64-*.AppImage
   ./sensetty-linux-x64-*.AppImage
   ```

### Android APK
1. Download `sensetty-android-*.apk` on your Android device.
2. Open the file to install (allow *"Install from unknown sources"* if prompted).

### Windows Portable
1. Download `sensetty-windows-x64-*.zip`.
2. Extract the archive and launch `sensetty.exe`.

---

## Key Features

### 🖥️ Multi-Protocol Terminal & Connectivity
- **SSH Terminal**: High-performance SSHv2 client with xterm-compatible terminal emulation, 256-color & truecolor rendering, key-based authentication, known host fingerprint verification, and automatic keep-alive.
- **Local Shell**: Direct access to local bash/zsh (Linux/macOS), PowerShell / cmd.exe (Windows), and Android local shell environment.
- **Serial Port (UART/COM)**: Full-featured serial terminal for hardware debugging (baud rates, data bits, parity, stop bits, flow control, hex send/receive, timestamping).
- **Industrial Protocols**: Built-in **Modbus TCP / RTU** master & slave testing utilities and raw TCP/UDP socket debuggers.
- **Split View & Multi-Tab**: Split terminal panes horizontally and vertically, duplicate tabs, and detach sessions.

### 🤖 AI Agent & Copilot
- **Multi-Provider AI**: Connect to **OpenAI (GPT-4o)**, **Anthropic Claude**, **DeepSeek-V3/R1**, **Ollama** (local models), and custom OpenAI-compatible APIs.
- **Terminal Context-Aware Diagnosis**: Capture recent terminal logs, errors, or selected text snippets into AI context with a single click.
- **Executable Command Extraction**: AI responses automatically detect terminal commands and provide one-tap execution buttons directly into your active shell.
- **Prompt Templates**: Built-in templates for error diagnostics, log analysis, bash script explanation, regex drafting, and shell command generation.
- **Adaptive UI**: Optimized two-column layout on desktop and adaptive tabbed view (`Chat` + `Context & Settings`) on mobile devices with zero keyboard truncation.

### 📱 Seamless Mobile & Desktop Experience
- **Adaptive Layout**: Responsive design transitioning from desktop multi-pane / split-screen navigation rails to mobile bottom navigation and touch-optimized gestures.
- **Mobile Touch Toolbar**: Dedicated mobile on-screen keyboard accessories for `Esc`, `Tab`, `Ctrl`, `Alt`, arrow keys, and command shortcuts.
- **Platform-Specific Optimization**: Tailored settings and features surfaced exclusively on supported platforms (Linux-specific windowing and shortcuts, Android background wakelocks and notifications).
- **Internationalization (i18n)**: Full native support for English and Simplified Chinese (简体中文) with instant language switching.

### 📁 Dual-Pane SFTP & File Manager
- **Remote & Local File Browser**: Dual-pane file manager for intuitive directory navigation, permissions management, file editing, and bulk operations.
- **In-Session SCP**: Direct drag-and-drop file upload and download within active terminal sessions.
- **Background Transfer Engine**: High-throughput file transfers with progress monitoring, cancellation, and retry handling.

### 🔌 Built-in MCP (Model Context Protocol) Server
- **Standardized AI Integration**: Native MCP server allowing external AI assistants (e.g., Claude Desktop, Cursor, Antigravity) to query server metrics, inspect session outputs, and execute verified shell commands.
- **MCP Inspector**: Real-time protocol visualizer and inspector for testing MCP tools, prompts, and resources.

### 🎛️ Real-Time Server Monitoring
- **System Metrics**: Monitor CPU load, memory utilization, disk I/O, and network bandwidth in real time.
- **Visual Dashboards**: Interactive metrics graphs powered by `fl_chart`.
- **Multi-Host Aggregation**: Pin multiple server nodes to a central dashboard for fleet monitoring.

### ⚙️ Session Management & Workspace Sync
- **Organized Sessions**: Group sessions into custom folders, assign color tags, icons, and connection profiles.
- **Export & Import**: Backup and restore sessions via encrypted or open JSON format.
- **Customizable Appearance**: Terminal color themes (Monokai, Solarized, Dracula, Nord, OneDark), customizable fonts, line heights, and cursor styles.

---

## Screenshots & Showcase

### Desktop Workspace
![Desktop Workspace](docs/ScreenShot.png)

### Mobile Experience
<div align="center">
<table>
  <tr>
    <td align="center"><b>Mobile SSH & AI Copilot</b></td>
    <td align="center"><b>Mobile SFTP File Manager</b></td>
  </tr>
  <tr>
    <td><img src="docs/Sensetty_Mobile_ssh_AI.jpg" width="380" alt="Mobile SSH and AI Agent" /></td>
    <td><img src="docs/Sensetty_Mobile_sftp.jpg" width="380" alt="Mobile SFTP File Manager" /></td>
  </tr>
</table>
</div>

### SFTP & File Transfer
![SFTP Dual Pane](docs/Session_SFTP.png)
*Dual-pane SFTP file management with drag-and-drop and directory synchronization.*

![In-Session SCP](docs/inSesseionSCP.png)
*In-session file upload and instant SCP transfer without leaving your shell.*

### Serial Port & Embedded Debugging
![Serial Port](docs/Session_SerialPort.png)
*Hardware serial port terminal with configurable baud rates, parity, and data framing.*

### Server Health Dashboard
![Server Monitor](docs/Monitor.png)
*Real-time server monitoring dashboard showing CPU, RAM, disk, and network stats.*

### MCP Server & Inspector
![MCP Server](docs/MCP_Server.png)
*Model Context Protocol (MCP) server status, tools registry, and stream inspector.*

---

## Keyboard Shortcuts

### Global Shortcuts
| Shortcut | Action |
|:---------|:-------|
| `Ctrl + T` | Open new terminal tab |
| `Ctrl + W` | Close active tab |
| `Ctrl + Tab` | Switch to next tab |
| `Ctrl + Shift + Tab` | Switch to previous tab |
| `Ctrl + Shift + F` | Toggle full screen workspace |
| `Ctrl + ,` | Open Settings |

### Terminal Shortcuts
| Shortcut | Action |
|:---------|:-------|
| `Ctrl + Shift + C` / `Ctrl + C` | Copy selected terminal text |
| `Ctrl + Shift + V` / `Ctrl + V` | Paste from clipboard |
| `Ctrl + +` / `Ctrl + -` | Zoom in / Zoom out terminal font size |
| `Ctrl + 0` | Reset terminal font size |
| `Ctrl + L` | Clear terminal scrollback buffer |

---

## Bug Reports & Feedback

If you encounter any issues or have feature requests, please submit an issue on the [Issue Tracker](https://github.com/tonyho/SenseTTY_release/issues).

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made with ❤️ by the SenseTTY Team

</div>
