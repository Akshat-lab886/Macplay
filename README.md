# 🎮 OpenPlay

> **The Free, Native macOS Gaming & Windows Compatibility Suite for Apple Silicon (M1–M4)**  
> *A fast, unified, zero-cost alternative to CrossOver and Parallels Desktop.*

[![Platform](https://img.shields.io/badge/Platform-macOS%2014.0%2B-blue.svg)](https://github.com/Akshat-lab886/OpenPlay)
[![Architecture](https://img.shields.io/badge/Architecture-Apple%20Silicon%20(ARM64)-brightgreen.svg)](https://github.com/Akshat-lab886/OpenPlay)
[![Metal](https://img.shields.io/badge/Graphics-Metal%203%20%2F%20D3DMetal-orange.svg)](https://github.com/Akshat-lab886/OpenPlay)
[![License](https://img.shields.io/badge/License-MIT-purple.svg)](https://github.com/Akshat-lab886/OpenPlay)
[![Release](https://img.shields.io/badge/Release-v1.0.0-success.svg)](https://github.com/Akshat-lab886/OpenPlay/releases)

---

## ⚡ What is OpenPlay?

**OpenPlay** bridges the gap between Windows PC software and macOS on Apple Silicon. It gives you the dual power of **Wine translation** (for high-speed, direct Metal gaming) and **Apple Native Virtualization** (for running full Windows 11 ARM64 virtual machines), completely free with no subscriptions.

```
       ┌────────────────────────────────────────────────────────┐
       │                   OpenPlay for macOS                   │
       └──────────────────────────┬─────────────────────────────┘
                                  │
         ┌────────────────────────┴────────────────────────┐
         │                                                 │
  [ Gaming & Apps ]                                [ Virtualization ]
  Wine 11.0 / CrossOver 26 Base                    Apple Virtualization.framework
  • D3DMetal (Apple GPTK 2)                        • Windows 11 ARM64 VM
  • DXVK + MoltenVK                                • VirtIO High-Speed Disk & Net
  • MSync (Mach Kernel Synchronization)            • USB Mass Storage Boot
  • 1-Click Game Launchers (Steam, Epic, GOG)      • Shared Folder Mounts
```

---

## 🌟 Key Features

### 1. 🕹️ Dual Graphics Pipeline: D3DMetal & DXVK
- **D3DMetal (Apple Game Porting Toolkit 2):** Direct translation of DirectX 11 and DirectX 12 calls straight into native Apple Metal 3 API with hardware ray-tracing support on M3/M4 GPUs.
- **DXVK + MoltenVK:** Direct Vulkan-to-Metal translation for DirectX 9, 10, and 11 compatibility.
- **Metal HUD:** Real-time in-game FPS counter, frame time graphs, GPU load, and memory usage.
- **AMD FSR 3 / 3.1 & Mod Support:** In-game FSR 3 and DLSS-to-FSR3 replacement mods run natively on Apple Silicon to double game framerates.

### 2. 🛍️ 1-Click Essential Apps Store
Download, configure, and launch essential PC stores and tools with authentic 512×512 Retina branding:
- **Game Launchers:** Steam Client for Windows, Epic Games Launcher, GOG Galaxy 2.0, Blizzard Battle.net, EA App, Ubisoft Connect.
- **Utilities & Tools:** 7-Zip (x64), Notepad++ (x64), VLC Media Player.
- **Automated Tuning:** OpenPlay automatically configures bottle registry keys, CSMT, Retina DPI scaling, and memory allocation.

### 3. 🎯 Curated Game Tuning Recipes
One-click performance profiles for popular PC titles:
- *Cyberpunk 2077* (Platinum) — D3DMetal + MSync + AVX2 translation
- *Elden Ring* (Gold) — D3DMetal + EAC offline tuning
- *Baldur's Gate 3* (Platinum) — D3DMetal + Vulkan / DX11 fallback
- *The Witcher 3: Wild Hunt Next-Gen* (Platinum) — DX12 D3DMetal profile
- *Grand Theft Auto V* (Platinum) — High-FPS DirectX 11 DXVK profile

### 4. 🖥️ Native Apple Virtualization (Parallels Alternative)
- Built on macOS native `Virtualization.framework` (`VZVirtualMachine`).
- Full support for **Windows 11 ARM64** with hardware-accelerated CPU and memory virtualization.
- Emulated USB Mass Storage boot for straightforward Windows ISO installation.
- Shared directory folders between macOS host and guest VM.

### 5. 🚀 Standalone macOS `.app` Generator
Convert any installed Windows game or software into an authentic macOS application bundle inside `~/Applications/OpenPlay/`. Launch your Windows games directly from Spotlight or your Mac Dock!

---

## 📥 Download & Installation

### Option 1: Direct Download (Recommended)
1. Go to the [**Latest Release**](https://github.com/Akshat-lab886/OpenPlay/releases/latest).
2. Download `OpenPlay-1.0.0-macOS-arm64.zip`.
3. Unzip and drag `OpenPlay.app` to your `/Applications` folder.

### Option 2: Command Line Tool (`openplay`)
OpenPlay includes a unified CLI binary for advanced users and automation:
```bash
# List and inspect bottles
openplay bottle list

# Run any Windows executable in a bottle
openplay run "GamingBottle" "path/to/game.exe"

# 1-Click install essential game launchers
openplay store install steam

# Check hardware and Rosetta status
openplay status
```

---

## 💻 System Requirements

| Specification | Requirement |
| :--- | :--- |
| **Operating System** | macOS Sonoma 14.0 or macOS Sequoia 15.0+ (Tested up to macOS 27) |
| **Hardware** | Apple Silicon Mac (M1, M1 Pro/Max/Ultra, M2, M3, M4) |
| **Memory** | 8 GB RAM minimum (16 GB+ recommended for AAA gaming) |
| **Storage** | 200 MB for OpenPlay; extra space for your games and bottles |

---

## 📄 License & Acknowledgments

- OpenPlay is licensed under the **MIT License**.
- Built using Apple Metal 3, Apple Virtualization.framework, Wine, DXVK, and Apple Game Porting Toolkit.

---
*Created with ❤️ for Mac gamers and developers.*
