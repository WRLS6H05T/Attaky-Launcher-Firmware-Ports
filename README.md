# WirelessGhost Firmware 👻
### Next-Generation Modular Wireless Recon & Input Platform for the Cyber Deck Plus

[![Target Chip](https://shields.io)](https://espressif.com)
[![Framework](https://shields.io)](https://platformio.org)
[![Hardware](https://shields.io)](https://github.com)
[![License](https://shields.io)](LICENSE)

**WirelessGhost Firmware** is a highly optimized, modular wireless reconnaissance and automation engine compiled specifically for the **Cyber Deck Plus** architecture (powered by the **Espressif ESP32-S3 dual-core 240MHz SoC with 16MB Flash and 8MB External PSRAM**). Deployed as a dynamic target binary, this firmware utilizes high-performance graphical subsystems and deep-level radio acceleration loops to deliver real-time environmental processing.

> ⚠️ **Disclaimer:** This project is developed strictly for educational purposes, authorized security auditing, and standalone defensive network monitoring. Please use responsibly and in compliance with your local laws.

---

## ⚡ Deployment & Launch Ecosystem

WirelessGhost Firmware sits natively within a versatile multi-boot ecosystem. Rather than wiping out the layout configuration or restricting the platform to a single runtime module, deployment utilizes an SD card storage paradigm managed directly by the primary system loader:

1. **Core Flash Layer:** The foundational **bmorcelli launcher (M5Launcher)** is flashed directly onto the ESP32-S3 device's onboard storage.
2. **SD Storage Array:** The compiled **WirelessGhost** tracking binary (`.bin`) along with companion environments like **Retro-Go** are loaded directly onto the root folder of the high-speed SD card.
3. **Dynamic Execution:** Using the **Attaky-Firmware-builder** framework parameters, the system boots into the main launcher graphical selection tree, enabling on-the-fly partition allocation, software installations, and modular execution choices.

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

This firmware configuration is precisely tuned to work with the following baseline specifications. Loading these modules onto standard boards without adequate external memory configurations will cause heap cap faults:

* **Microcontroller:** Espressif ESP32-S3 (Xtensa Dual-Core LX7, 240MHz).
* **Memory Configuration:** 16MB Flash Allocation / **8MB External PSRAM (Strictly Required)** for NimBLE scan tables.
* **Display Driver Compatibility:** Integrated SPI LCD Controllers with Touch Interface overlays managed via unified registry calls.
* **Radio Interface Support:** Standalone 2.4GHz internal antenna array with localized hook registers for external transceiver expansion modules.

---

## 🚀 SD Target Setup & Installation Deploys

Because the execution targets sit inside the dynamic multi-boot structure of the custom partition launcher, flashing procedures differ from standalone scripts:

### 1. Flash the Primary Multi-Boot Launcher
Use the web flasher tool interface or platform CLI options to commit the base launcher system binary framework onto the core ESP32-S3 internal block storage partition array.

### 2. Stage Assets on the Local SD Card Storage
Insert your micro SD module into your development workstation environment and structure the root partition tree exactly as follows:
```text
/ (SD Card Root)
├── wirelessghost_v0.1.0.bin
└── retro_go_launcher.bin
```

### 3. Execution & Run Phase via Launcher Core
Mount the indexed SD storage target directly onto your **Cyber Deck Plus** peripheral slot array and power up the machine. Use the graphical UI matrix controls to launch, partition, install, or refresh the firmware binaries smoothly on execution.

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
* **Hardware Kits:** Pre-assembled, custom-branded physical device arrays pre-flashed with stable firmware builds are available periodically on our project dashboard.

---
Developed by **WirelessGhost** 👻 • Built for the Portable Hardware Community.
