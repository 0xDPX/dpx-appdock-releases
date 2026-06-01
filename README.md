# DPX AppDock releases

Public update feed for **DPX AppDock** (source code is maintained in a private repository).

This repo contains **no application source code** — only installers, update packages, and the manifest the app checks for new versions.

## Download

| File | Purpose |
| --- | --- |
| [DPX.AppDock-1.0.0-setup.exe](https://github.com/0xDPX/dpx-appdock-releases/releases/download/v1.0.0/DPX.AppDock-1.0.0-setup.exe) | First-time install (Windows 10/11, x64) |
| [DPX.AppDock-1.0.0-win-x64.zip](https://github.com/0xDPX/dpx-appdock-releases/releases/download/v1.0.0/DPX.AppDock-1.0.0-win-x64.zip) | In-app update package (used by existing installs) |

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

## Version 1.0.0

First public release. Highlights:

- Compact matte dock for apps, folders, files, and websites
- Groups with expandable dock bar, drag-and-drop organization
- Auto-hide, per-monitor placement, global hotkeys, running indicators
- In-app updates with SHA-256 verification
- Settings backup/import and a multi-page welcome guide

Full release notes are included in each [GitHub Release](https://github.com/0xDPX/dpx-appdock-releases/releases) description.

## Maintainers

Publish a new version from the private source repo:

```powershell
.\scripts\Publish-Release.ps1 -Version 1.0.0
$env:GITHUB_TOKEN = "<token with write access to this repo>"
.\scripts\Publish-UpdateFeed.ps1 -Version 1.0.0 -ReleaseNotes "See release notes."
```

See the private source repo’s `releases/RELEASE.md` for the full publish workflow.
