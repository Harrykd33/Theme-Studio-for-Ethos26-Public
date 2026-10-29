# Theme Studio for Ethos

A portable Windows app for previewing and installing themes on FrSky radios running **Ethos 26.x**. Also install optional scripts, convert model images and add WAV audio over USB.

## Getting started

1. Open `ThemeStudioForEthos.exe` from the extracted release or local `dist/` folder. Python is not required.
2. Connect your radio in **USB storage / SD card** mode.
3. Select its detected drive, or browse to the folder containing `radio.bin` and `models/`.
4. Preview and select themes. Add optional scripts or local files as needed.
5. Choose **Review & install** and confirm the changes.
6. Eject the drive, disconnect and restart the radio. Select a theme under **System > General > Theme**.

For Windows SmartScreen prompts, see the [first-launch guide](updater/FIRST-LAUNCH.txt).

A short tutorial opens on first launch. Skip it any time, or replay it from **Help & About > Run tutorial**.

## Features

- **Theme previews:** Dashboard and Model views, filters and saved favorites.
- **Auto Update:** Themes and packages update automatically. The badge is a status label. Available local files support offline use.
- **Optional scripts:** Install packages such as [Heli Model Wizard](https://github.com/Harrykd33/Ethos-RF-Model-Wizard), or add a local script folder/ZIP.
- **Model images:** Remove backgrounds, adjust cropping and preview at 1:1. Export BMPs at **300 x 280** (Ethos standard) or **280 x 300** (kevd theme). Image names allow up to 11 characters.
- **Audio:** Add WAV files, folders or ZIPs to a selected radio voice folder. Supported WAV formats are converted automatically when needed.
- **Help & About:** App releases, setup guidance and advanced update options at the bottom of the scrolling help.

## Installation notes

Installing themes replaces `scripts/Themes/` with your selection. Unselected themes in that folder are removed; no backup is kept after a successful install. Include favorites during review if you want to keep them.

Script packages replace only their own folders. Audio and model images add files; audio conflicts offer **Skip file**, **Skip all** or **Cancel install**. Other scripts, models and radio settings are preserved.

Local uploads stay queued during updates but are not saved when the app closes. Review all changes before installing.

See the [technical guide](updater/README.md) for building the app, publishing catalogs and installation details.

## License

[GNU General Public License v3.0](LICENSE).
