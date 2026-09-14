# WirelessGhost Firmware and Attaky ports 👻
### Next-Generation Modular Wireless Recon & Input Platform for the Cyber Deck Plus

[![Target Chip](https://shields.io)](https://espressif.com)
[![Framework](https://shields.io)](https://platformio.org)
[![Hardware](https://shields.io)](https://github.com)
[![License](https://shields.io)](LICENSE)

**WirelessGhost Firmware** is a highly optimized, modular firmware framework built from the ground up for portable security reconnaissance and structural automation. Engineered specifically for the **Cyber Deck Plus** architecture (powered by the **Espressif ESP32-S3 dual-core 240MHz SoC with 16MB Flash and 8MB External PSRAM**), this operating system leverages high-performance graphical engines and deep-level hardware acceleration to provide real-time environment telemetry.

> ⚠️ **Disclaimer:** This project is developed strictly for educational purposes, authorized security auditing, and standalone defensive network monitoring. Please use responsibly and in compliance with your local laws.

---

## ✨ Project Core Philosophy

Unlike monolithic firmware setups that easily saturate microcontroller heaps, WirelessGhost Firmware treats features as decoupled modules. It isolates low-level driver processes from wireless radio stacks, preventing memory leaks, watchdog resets, and kernel panics when driving intensive Bluetooth (`NimBLE`) and Wi-Fi (`lwIP`) subroutines simultaneously.

---

## 📊 Feature Matrix & Implementation Roadmap

WirelessGhost Firmware is divided into structural phases to ensure low-level driver stabilization before running massive background tracking operations.

### ✅ Phase 1: Core System & Display Engine
* **Universal Graphics Routing:** Built using the `M5Unified-attaky` and `M5GFX` rendering layers for optimized frame buffer scaling across distinct screen modules.
* **Peripheral Bus Debouncing:** Pre-configured mapping profiles for integrated hardware peripherals, including core Gamepad states, split Keyboard matrices, and automated Battery/Fuel Gauge status indicators.
* **Local Storage Array:** Fully integrated SD Card management routines with operational toolbar indicator iconography to verify connection states on structural boot.
* **RGB System Telemetry:** Fully programmable RGB LED matrix management scripts supporting active animation modes across peripheral gamepad and keyboard components.

### ➡️ Phase 2: User Interface & Visual Theming
* **Identity Branding:** Custom `WirelessGhost` splash animation matrices deployed securely at the bootup transport layer.
* **Thematic Palettes:** Built-in UI palette registers allowing immediate layout shifts across multiple profile settings:
  * 🟩 `Matrix` (Classic terminal green)
  * 🟧 `Amber` (High-contrast industrial neon)
  * 🟦 `Ocean` / `Slate` (Low-fatigue utility tones)
  * 🟥 `Crimson` / `Violet` (Tactical dark modes)
* **Real-time Status Bar:** Dynamic layout blocks rendering structural task execution data, channel hop indicators, and hardware battery percentages directly in the display header.

### ➡️ Phase 3: Wireless Reconnaissance Restructuring
* **Hierarchical Scanning Architecture:** Complete migration from simple network lists to structured relational maps separating **Access Points ➡️ Connected Stations ➡️ Active Clients** in precise hierarchy.
* **Advanced Packet Analysis Platform:** Structural framework updates changing basic sniffing subroutines into focused reconnaissance tools with targeted list selection models:
  * `Connect` / `Activity Monitoring` / `Tracking Telemetry`
* **Defensive Honeypots:** Isolated initialization loops and flexible file templates designed to simulate beacon environments for security audits.

### ➡️ Phase 4: Persistence, Privacy & Defensive Tools
* **Network Credential Persistence:** Secure internal storage parsing to save localized Wi-Fi configurations for automated profile reconnection on initial boot.
* **Tactical Privacy Masking:** High-security display routines built to abstract active identity values on the display layer, leaving only initial index characters visible (`Privacy Masking Mode`).
* **BLE Environmental Mapping:** Real-time background telemetry loops monitoring structural packet frequency rates, parsing target device types and tracking unique signal bursts.

### ➡️ Phase 5: Geolocation Mapping & Hardware Phantom Modes
* **API Integration Matrix:** High-performance telemetry serialization protocols designed to connect background mapping pipelines seamlessly into industry-standard mapping platforms:
  * `Wiggle API` / `Wardrive.go API` / `WatchDogsGoWars API`
* **Modular Payload Transports:** Hardened deployment wrappers optimizing keystroke payload execution stability (`BadUSB/Live Pad`), cleanly isolated from active radio modules to ensure data delivery without transmission drops.

---

## 🛠️ Hardware Specification Requirements

This operating system is precisely tuned to work with the following baseline specifications. Loading these modules onto standard boards without adequate external memory configurations will cause heap cap faults:

* **Microcontroller:** Espressif ESP32-S3 (Xtensa Dual-Core LX7, 240MHz).
* **Memory Configuration:** 16MB Flash Allocation / **8MB External PSRAM (Strictly Required)** for NimBLE scan tables.
* **Display Driver Compatibility:** Integrated SPI LCD Controllers with Touch Interface overlays managed via unified registry calls.
* **Radio Interface Support:** Standalone 2.4GHz internal antenna array with localized hook registers for external transceiver expansion modules.

---

## 🚀 Building & Flashing

This project is configured natively for **PlatformIO**. It integrates with the `arduino-esp32 v3.x` core and uses advanced compiler flags to optimize code placement within the fast internal RAM (`IRAM`).

### 1. Clone the Architecture Repository
```bash
git clone https://github.com/WirelessGhost-OS.git
cd WirelessGhost-OS
```

### 2. Verify Your Configuration Pack
Ensure your localized configuration matches your device deployment environment inside your configuration profiles:
```ini
[env:cyber-deck-plus]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino
board_build.partitions = default_16MB.csv
build_flags = 
    -DBOARD_HAS_PSRAM
    -DARDUINO_USB_CDC_ON_BOOT=1
```

### 3. Build and Upload
```bash
# Compile and flash binary via localized PlatformIO CLI channels
pio run --target upload
```

---

## 🤝 Credits & Acknowledgments

This project relies upon and is deeply indebted to the foundational work of the following developers in the open-source hardware community:

* **B Morcelli:** For the foundational **bmorcelli launcher source code (M5Launcher)**, providing essential partition management mechanisms, modular execution structures, and core multi-firmware loading foundations.
* **Attaky-Firmware-builder:** For providing the structural compilation environment, layout build configurations, and localized platform toolchains that make the Cyber Deck Plus ecosystem possible.
* **OpenCode / Zen / Big Pickle:** For architectural AI code collaboration, structural modular logic optimizations, and backend roadmap refinement.

---

## 👥 Community and Contribution

I built WirelessGhost Firmware as an open platform to empower makers and independent hardware developers. I love community involvement!

* **Bug Tracking & Reporting:** If you hit memory errors or identify pin mismatch bugs inside specialized graphics configurations, please open an Issue with complete core dump logs attached.
* **Feature Development Tiers:** I encourage developers to fork my Phase layers and build clean pull requests targeting single, modular feature files.

---

## 🪙 Support the Project

WirelessGhost Firmware is, and always will be, free and open for independent makers. If this firmware has saved you time on your hardware build, helped you learn microcontroller engineering, or looks amazing on your custom deck screen, consider supporting development:

* **Patreon:** Join my developer tier to get access to early-compiled alpha binaries of upcoming Recon modules before they drop publicly.
* **Buy Me a Coffee:** Support my monthly token and hardware testing budget with a simple one-time contribution.
* **Hardware Kits:** Pre-assembled, custom-branded physical device arrays pre-flashed with stable firmware builds are available periodically on my project dashboard.

---
Developed by **WirelessGhost** 👻 • Built for the Portable Hardware Community.
