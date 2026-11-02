B-Morcelli themed for the Attaky.

This release features a complete visual re-theme based on the original work by b_morcelli, now fully redesigned to match the Attaky theme aesthetic. Flash from the Attaky website or via esp-tool. The bin is there for personal customization.

## Latest build

**Attaky_Launcher_V0.1.5.bin** - merged image for the 16 MB flash.

    esptool --port COMx write_flash 0x0 Attaky_Launcher_V0.1.5.bin

The Launcher lives in the 1.5 MB test partition at `0x30000`, so a Launcher-only update can be flashed straight to `0x30000` instead of the whole image. Writing the merged image rewrites NVS: settings are re-read from `config.conf` on the SD card, but anything kept only in NVS goes back to defaults.

### What V0.1.5 changes over A001

- **Eight palettes** - Attaky, Attaky Dark, Black, Green, Orange, Purple, Green Dark and Blue Dark. The colour-named ones use a light grey page with dark grey text, the "Dark" ones a black page with the same accent as neon, and Attaky follows the colours used on attaky.com.
- **Carousel rework** - the selected item is one large square tile in the middle with smaller neighbours either side, labels are clipped to their tile instead of running off the panel, and each theme keeps to its own accent on the page and grey side tiles.
- **Boot splash** - the Attaky mark and wordmark sit centred above "Launcher" over the matrix rain. The rain starts on a clean screen, falls as rain rather than typing on, and can be switched off in Config.
- **Battery gauge** - top right of the menu, read from the MAX17048 fuel gauge over I2C.
- **Front keys** - the 4-way pad moves by row and column in the menu instead of walking a flat index (`BOARD_4WAY_NAV`).
- **Touch** - orientation corrected for the 180 degree mounted panel.

## What is in this repo

| File | What it is |
| --- | --- |
| `Attaky_Launcher_V0.1.5.bin` | Current merged Launcher image (16 MB layout) |
| `Attaky_Launcherv0.1.0_A001.bin` | First Attaky Launcher release |

The rest are app firmwares for the SD-card installer (Gameboy, Pomodoro, TXT, Voice Memo, Plane Radar, Music Machine, Denki Kurage, MicroPython, WirelessGhost, the Attaky Controller and the mesh builds), plus a few older images kept for reference.

## Features

**Carousel UI:** Re-skinned user interface elements, menus, and color palettes from the b_morcelli base to the Attaky design, converting the main UI into a smooth carousel navigation.

**Multi-Firmware Booting:** Allows you to launch multiple firmwares directly from the SD card that fit within the b_morcelli partition layout.

**Firmware Compatibility Note:** Current firmwares available in the store will not launch if they are just merged. They must be reworked using the firmware builder, or you can develop entirely new firmware designed to launch from this platform.

**Retro-Go Optimization:** The full Retro-Go package is too large to load with all consoles included. It needs to be split into single consoles or a small custom group of your liking.

Place your choice of bin files on an SD card and install and launch to use the firmware. Can be used with multiple SD cards.

## Removed

**OTA updates** have been removed for now, and will be added back once fully functional.

**Charge configuration** has been removed from Config.

## Next fixes

- UI boundaries for removal of firmware
- Smoother transitions between apps
- Customizable UI

## Thanks

Thanks to the Attaky firmware builder and Opencode.
Thanks to the open source B-Morcelli launcher for a platform to build on for makers and open source projects.

W1R3L3556H05T
