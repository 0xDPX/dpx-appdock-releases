# DPX AppDock — Windows releases

Public download page for [DPX AppDock](https://dpx-labs.com/appdock), a Windows dock for launching apps, folders, files, and web shortcuts.

This repo holds the installer builds and the update manifest the app checks for new versions. Source code is not published here.

## Download

**Latest:** [DPX AppDock v1.0.0](https://github.com/0xDPX/dpx-appdock-releases/releases/latest)

| File | Use |
| --- | --- |
| `DPX.AppDock-{version}-setup.exe` | First-time install (recommended) |
| `DPX.AppDock-{version}-win-x64.zip` | In-app updates only |

## Requirements

- Windows 10 version 1607 or later, or Windows 11 (64-bit)
- Microsoft [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0) (x64)

The setup installer checks for the runtime and installs it if needed.

## After install

Settings and your dock layout live in `%AppData%\DPX.AppDock\`. Uninstalling from Windows Settings removes the program files; you can choose whether to keep that folder.

Updates can be checked from the app (Settings → About, or the tray menu). This repo’s `update-manifest.json` is what the app reads to know when a newer build is available.

## Links

- Product page: [dpx-labs.com/appdock](https://dpx-labs.com/appdock)
- Releases: [github.com/0xDPX/dpx-appdock-releases/releases](https://github.com/0xDPX/dpx-appdock-releases/releases)

Questions or feedback: reach out through [DPX Labs](https://dpx-labs.com/).
