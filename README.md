# DPX AppDock releases

Official download and auto-update feed for **DPX AppDock** on Windows.

This repository hosts installers, in-app update packages, and the manifest the app checks for new versions.

## Download

| File | Purpose |
| --- | --- |
| [DPX.AppDock-1.0.1-setup.exe](https://github.com/0xDPX/dpx-appdock-releases/releases/download/v1.0.1/DPX.AppDock-1.0.1-setup.exe) | First-time install (Windows 10/11, x64) |
| [DPX.AppDock-1.0.1-win-x64.zip](https://github.com/0xDPX/dpx-appdock-releases/releases/download/v1.0.1/DPX.AppDock-1.0.1-win-x64.zip) | In-app update package (used by existing installs) |

**Requirements:** Windows 10 or 11 (64-bit). The setup installer installs the Microsoft .NET 8 Desktop Runtime automatically when it is not already present.

## Auto-update

The installed app reads [`update-manifest.json`](update-manifest.json) from this repository on startup (if enabled) and from **Settings → About → Check for updates**.

Each manifest entry includes:

- `version` — semver compared to the installed app
- `downloadUrl` — direct link to the `.zip` update package
- `sha256` — required hash verified before install
- `releaseNotes` — shown in the update dialog

Manifest URL (configured in the app):  
`https://raw.githubusercontent.com/0xDPX/dpx-appdock-releases/main/update-manifest.json`

## Version 1.0.1

Group dock polish: centered expand panel, in-group reorder animations, stable panel during drags, Explorer drops onto groups, along-edge placement, and dialogs positioned beside the dock.

Full release notes are included in each [GitHub Release](https://github.com/0xDPX/dpx-appdock-releases/releases) description.
