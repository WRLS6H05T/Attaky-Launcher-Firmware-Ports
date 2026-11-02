B-Morcelli themed for the Attaky.
This release features a complete visual re-theme based on the original work by b_morcelli, now fully redesigned to match the Attaky theme aesthetic.
Flash from the Attaky website or via esp-tool

Latest build: Attaky_Launcher_V0.1.5.bin
---------------------------------------
Merged image for the 16 MB flash. Write it at 0x0 (`esptool --port COMx write_flash 0x0 Attaky_Launcher_V0.1.5.bin`) or flash it from the Attaky website.

The Launcher lives in the 1.5 MB test partition at 0x30000, so a later Launcher-only update can be flashed to 0x30000 instead of the whole image. Flashing the merged image rewrites NVS with blanks; your settings are re-read from config.conf on the SD card, but anything stored only in NVS resets.

What V0.1.5 changes over A001:

- Eight UI palettes (Attaky, Attaky Dark, Black, Green, Orange, Purple, Green Dark, Blue Dark). The colour-named ones use a light grey page, the "Dark" ones a black page with the same accent, and Attaky follows the palettes on attaky.com.
- Carousel menu reworked: the selected item is one large centre tile with smaller neighbours either side, labels are clipped to their tile instead of running off the panel, and each layout keeps a single accent colour on the page and grey side tiles.
- Boot splash: the Attaky mark and wordmark are centred above "Launcher" over the matrix rain. The rain starts clean, falls as rain rather than typing on, and can be switched off in Config.
- Battery gauge in the top right, read from the MAX17048 fuel gauge over I2C.
- Front keys use the 4-way pad for row/column movement in the menu (BOARD_4WAY_NAV).
- Touch orientation corrected for the 180 degree mounted panel.
- Config: the charging section is removed and the Web UI entry is now labelled APP UI.

The bin is there for personal customization.

Key Updates

Carousel UI: Re-skinned user interface elements, menus, and color palettes from the b_morcelli base to the Attaky design, converting the main UI into a smooth carousel navigation.

Multi-Firmware Booting: Allows you to launch multiple firmwares directly from the SD card that fit within the b_morcelli partition layout.
Firmware Compatibility Note: Current firmwares available in the store will not launch if they are just merged. They must be reworked using the firmware builder, or you can develop entirely new firmware designed to launch from this platform.

Retro-Go Optimization: The full Retro-Go package is too large to load with all consoles included. It needs to be split into single consoles or a small custom group of your liking.

Temporary Removal:
OTA updates have been removed for now (will be added back once fully functional).
Permanent removal:
The charge configuration option has been removed.

Place your choice of bin files on a sd card and install and launch to use the firmware
Can be used with multiple sd cards.
NEXT FIXES
UI boundries for removal of fimware
Smoother transitions between Apps
Customizable UI

Thanks to the Attaky firmware builder and Opencode. 
Thanks to the open source B-Morcelli launcher for a platform to build on for makers and open source projects.
W1R3L3556H05T
