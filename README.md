# Theme Studio for Ethos

Theme Studio for Ethos is a portable Windows desktop app for browsing,
previewing and installing themes on FrSky radios running Ethos 26.x. Choose a
palette, preview its appearance and install your selected themes over USB.
The app also installs optional script packages, including Heli Model Wizard.

## Features

- **Live palette previews:** Preview the Dashboard and Model menu before installing.
  The screens alternate automatically every three seconds when you preview or
  select a theme. Choosing a screen manually restarts the three-second timer.
- **Theme filters:** Browse Dark, Light, All Themes or Favorites, with selections preserved
  as you switch filters.
- **Favorites:** Star themes to save them in Favorites. In the installation review,
  choose **Keep favorite themes with this install** to include available starred
  themes alongside your selection. Favorites and this option are remembered.
- **USB installation:** Detect Ethos storage automatically or select it manually.
- **Transfer progress:** Follow downloads, file verification and installation.
- **GitHub catalogs:** Refresh available themes and published script packages
  without rebuilding the app.
- **Bundled themes:** Use the included theme catalog when GitHub is unavailable.
- **Optional scripts:** Select script packages separately from themes, or install
  scripts on their own.
- **Separate package columns:** Themes and optional scripts stay visible together.
- **Automatic radio detection:** Connected storage is checked in the background,
  with its volume name and free space shown when available. A three-second toast
  announces a newly detected radio, and its ready status turns yellow.
- **Installation review:** See themes being added, replaced and removed before
  confirming. Installed themes are marked when the radio is connected.
- **Space check:** The combined themes and scripts are checked against available
  space before any package is written, including allocation and working space.
- **Saved preferences:** Window size, filter, preview and selections are remembered.
- **Help and diagnostics:** Check published app releases from Help & About and
  copy activity details locally for troubleshooting.

## Getting started

You need a Windows PC and an Ethos 26.x radio connected in USB storage / SD card
mode. The packaged executable does not require Python. Internet access is
required to refresh GitHub catalogs or download script packages.

1. Open `dist/ThemeStudioForEthos.exe` from a local build or extracted app package.
2. Connect your radio over USB and choose **storage / SD card** mode.
3. Select the detected Ethos storage drive, or browse to its root folder. The
   correct drive contains `radio.bin` and a `models/` folder.
4. Click a theme thumbnail or **Preview** to see its appearance, then check the
   themes you want to keep. Optionally select entries in **Script Packages**.
5. Click **Review & install**, review the destination and selected
   packages, then confirm. Keep the radio connected until installation finishes.
6. Eject the drive in Windows, disconnect and restart the radio. Choose your
   installed theme under **System > General > Theme**.

The unsigned portable executable may trigger Windows SmartScreen on first
launch. See [the first-launch guide](updater/FIRST-LAUNCH.txt), also included
beside the built executable as `READ-ME-FIRST.txt`.

Previews approximate the radio's appearance. The app does not detect firmware
compatibility or flash firmware; confirm your radio is running Ethos 26.x.

## How installation works

Theme installation replaces `scripts/Themes/` with the selected themes and their
PNG assets. Previously installed themes in that folder that are not selected,
obsolete images and compiled Lua files are removed. No backup is retained after
a successful installation. Other scripts, models and radio settings are left alone.

The app stages and verifies new files before activating each package. Script
packages replace their own folders under `scripts/`; unselected script packages
are left alone. See the [installation details](updater/README.md) for recovery
behavior and package-specific requirements.

## Optional script packages

Select **Heli Model Wizard** in the **Script Packages** column to install the
standalone package from
[Ethos-RF-Model-Wizard](https://github.com/Harrykd33/Ethos-RF-Model-Wizard).
It can be installed alone or alongside themes. **Select all** selects themes
only, so script packages must be selected explicitly.

The published script list is managed through
[script-packages.json](script-packages.json). Repository owners can publish
catalog changes to public GitHub `main`; users receive the updated list with
**Refresh GitHub** or when reopening the app. Adding packages to the catalog
requires repository write access. See the
[script catalog instructions](updater/README.md#owner-controlled-script-catalog)
for the entry format and publishing helper.

## License

This project is licensed under the [GNU General Public License v3.0](LICENSE).
