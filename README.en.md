# Nikon Z6 Custom Shutter Sound

Version: 2026-10-08. For the Nikon Z6 only, based on firmware C3.80.

Provides separate Chinese or English shutter sound menus, card-based sound replacement, four numbered sound slots, preview playback, and reloading. The selected sound number and on/off setting are saved on the card. During continuous shooting, each shot starts playback from the beginning, cutting off the previous sound. Separate opening and closing sounds for long exposures have not been implemented.

## Package Contents

Located in `z6/Custom shutter sound自定义快门声/`:

- `cn/SHCORE.BIN`: Chinese menu core, paired with `EG162080.BIN` at the package root.
- `en/`: Matching English `EG162080.BIN` and `SHCORE.BIN` files.
- `EG162080.BIN`: Main firmware for the Chinese version.
- `SHUTTER.WAV`: Default sound example for the card.
- `SHUTTER/1.WAV` through `4.WAV`: Four sound examples: 1 — a cat; 2 — the shutter of a film camera; 3 — a bird; 4 — the leaf shutter of a Soviet camera.
- `SOUND_SPEC.en.md`: Sound format, naming, and preparation requirements.

## Installation and Use

1. Back up the existing settings-related files on the card. *It is recommended to move your photos off the card, then back up all files and folders at the card root.*
2. For Chinese, copy the package-root `EG162080.BIN` and `cn/SHCORE.BIN` to the card root. For English, copy both BIN files from `en/` to the card root. Also copy the package-root `SHUTTER.WAV` and the `SHUTTER` folder to the card root. On the camera, start the update from **Firmware version**. Do not interrupt power during the update. Use a sufficiently charged battery as required by Nikon's firmware update instructions.
3. After the update, turn the camera off and back on. Wait about five seconds after startup and until the card access indicator goes out, then open the shutter sound settings in the setup menu to enable the feature, select a sound number, or play a preview.
4. To change a sound, replace the corresponding WAV file, then select its number or use **Reload**. There is no need to flash the firmware again.
5. *Please note*: The added menu supports only the directional buttons. The touchscreen and OK button cannot be used in this menu.

## Usage Notes

Update the firmware first. Once you have followed the installation steps, you can explore the feature. The custom shutter sound settings appear below **Firmware version** in the setup menu. *A cut-off meow after startup is normal.*

After trying the feature, turn the camera off and remove the card. Follow the requirements in `SOUND_SPEC.en.md` to replace sounds 1–4 with your own shutter sounds. You may use fewer than four numbered sound files, but do not add more than four.

## Disabling and Restoring

Turning the feature off in the menu only disables custom sounds during shooting. Turning the camera off, removing `SHCORE.BIN`, and turning it back on activates the missing-core fallback path.

To restore the complete stock firmware, use Nikon's official Z6 firmware and follow Nikon's official update procedure.

## Disclaimer

The author accepts no responsibility for issues after installation, including a bricked camera or freezes. The author can only state that these issues have not occurred on their own camera.

## Matching File Hashes

### cn

firmware_sha256: 5fc400199d782feaccfa530865303cc652b3f48891838599101909081984b976
core_sha256: 5f2e14ed53b78bd00bff077028781252c29f6a94a12eb529b438e0904a91d6d2

### en

firmware_sha256: 796806291185953ceaa9e59c428e844b2e6d5b11f5af739794c70ccc9d346c1a
core_sha256: 88aecb623a057418bba65c67fbc3cdd95cef3eaa612a39358d19493beee8f754
