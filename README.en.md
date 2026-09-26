# Game Bub Rev4 zh-dark (red·steve) Release Notes

**[中文](README.md) · [English](README.en.md)**

> Chinese custom firmware based on the official [Game Bub](https://github.com/elipsitz/gamebub) v1.0.2 (commit `e779b7c`).
>
> This repo **publishes release notes only**, viewable without a GitHub login. Firmware binaries are not provided here.

---

## Official Baseline
- **v1.0.2**: Official release; this custom series is derived from it (English UI, official themes, official sounds and wallpaper logic).

## zh-dark35 (Latest)

- **Scanline filter**: Added a 10th in-game filter, "Scanlines" (retro LCD row darkening, fixed strength 6/15, applied after color correction); the FPGA side adds a `ScanlineFilter` module and control register 0x1018; the MCU side adds `set_scanline` / `configure_filter`.
- ⚠️ This build's UF2 still bundles the official bitstream, so selecting "Scanlines" has no visual effect yet (no crash/error); it will take effect with a future bitstream build.
- **Render logging**: Only logs a frame when rendering exceeds 25 ms, reducing serial spam and slightly easing desktop stutter.
- **Version / docs**: README download section updated to .35; the "Return to official release" note adds the SD-card `official UF2` folder path.

## zh-dark34

- **Wallpaper list**: Removed the "Close wallpaper" item; the first item is now "Clear rotation list"; entering wallpapers auto-locates the currently rotating one; the rotation check mark changed from X to a red dot.
- **Favorite shortcut**: Changed from "X+A" to "Y+A" (hold Y, then A).
- **Hint sounds**: The low-frequency hint tone was lowered further (180–460 Hz), more muffled, with a clearer distinction from the crisp tone.
- **USB card reader / cartridge mode**: Exit no longer reboots the device (SD-card behavior to be verified on real hardware).
- **Button guide**: The wallpaper page hint bar was redrawn with official-style icons; added 11 button icons (Y, D-pad, Start, Select, L, R, power, volume).
- **Tools menu**: Added a "Return to official release" entry (safe, guided flow; does not auto-flash).

## zh-dark27 ~ zh-dark33

### zh-dark33
- Thumbnail low-memory fallback handling.
- Per-image independent position / scale / layer stored.
- Rotation selection inside the large preview; cohesive UI sound effects; background conversion tool.

### zh-dark32
- Wallpaper list thumbnails + numbers.
- Large preview: position / scale / front-back layer adjustment.

### zh-dark31
- Lower-pitched output improved, frequency 240–660 Hz.
- Boot favorite: can auto-launch a fixed slot game; hold Home to skip.
- Wallpaper tool changed to "crop the transparent border first, then convert".

### zh-dark30
- Menu sounds: low / crisp two styles + three intensity levels, off by default.
- Distinguishes navigation / confirm / back / action / error sounds.

### zh-dark29
- First-boot language selection (简体中文 / English).
- Fixed crash when pressing B on the search page (RefCell double borrow).
- ROM-list input response optimized.

### zh-dark28
- Core-page layout and focus-path fixes; fixed a focus issue matching "core page lockup".
- Favorite operation unified to X+A; a small heart is shown at the bottom center.
- Added a low-memory streaming PNG path for the wallpaper conversion tool.

### zh-dark27
- Wallpapers & favorites: four favorite slots below the core page; in the ROM list, hold X+A to add/remove favorites.
- Favorite launch: select a slot and press A; auto-launches GB/GBC/GBA by extension.
- Full-slot warning, no auto-overwrite; slots do not support drag reordering.

## zh-dark21 ~ zh-dark26
### zh-dark26 ~ zh-dark25
- No per-version record (transitional; zh-dark27 builds on 26).
### zh-dark24
- Redrew the body outline based on the official landscape shape; removed menu/game categories and three-page paging; merged to a single page.
### zh-dark23
- Search moved into the core list, restoring the external four options; added settings / in-game button guide.
### zh-dark22
- Added global search with no preselected core, temporarily placed on the main menu.
### zh-dark21
- English word-abbreviation and Chinese substring rules, plus a root-directory search fix; added a scan-status hint.

## zh-dark11 ~ zh-dark20
### zh-dark20
- Chinese/English switching with restart confirmation.
### zh-dark19
- First pinyin search, background-limited scan.
### zh-dark18
- About page adds thanks to the Furries localization.
### zh-dark17 ~ zh-dark16
- Theme now shows a restart menu after pressing A; repeated A can trigger it; the reddish tone was slightly pulled back after enhancing dark red.
### zh-dark15
- Merged retro yellow X, retro saturation, and "winterless red" / original themes.
### zh-dark14
- Not released as a standalone build.
### zh-dark13
- K palette experiment (briefly replaced slot 6, later restored retro yellow and split it into a separate option).
### zh-dark12
- First "retro yellow" color grade.
### zh-dark11
- About page adds STEVE 没有冬, version, and time; a confirmed-stable rollback version.

---

*In the beginning, this was just a UI designer who had never used an AI tool.*

## zh-dark1 ~ zh-dark10 (Early foundation)
### zh-dark10
- Fixed missing refresh after natural input, page-switch display state, and the Chinese-directory-limit hint.
### zh-dark9
- Fixed focus handoff where the D-pad / A became inactive after the animation ended.
### zh-dark8
- Black-background white-to-red gradient animation, persistent red logo, partial refresh and input scheduling optimization; a boot focus issue was discovered later.
### zh-dark7
- Nine-row candidate list, longer Chinese ROM names, line-by-line scrolling and per-entry drawing.
### zh-dark6 ~ zh-dark5
- Limited list-render memory, clarified core identity and suffix filtering, fixed B-back and loading-hint paths, and adjusted the final stack budget.
### zh-dark4
- Candidate fix for the core-load crash via stack space and stack-overflow diagnostics.
### zh-dark3 ~ zh-dark1
- Chinese and dark-interface experiments on the landscape official baseline; handled early boot, Chinese font, and background issues.

---

> This repo provides release notes only, no firmware download. Based on [elipsitz/gamebub](https://github.com/elipsitz/gamebub) v1.0.2; licensed under GPL v3 and CERN OHL-S.
