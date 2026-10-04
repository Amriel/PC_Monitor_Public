# PC Monitor — releases

Installer releases of **PC Monitor**, a local resource monitor for Windows.

This repository contains only release files — no source code.

Each release has two files:

- `PCMonitor-Setup-X.Y.Z.exe` — the installer (per-user, no admin rights needed to install);
- `PCMonitor-Setup-X.Y.Z.exe.sha256` — its SHA-256 checksum.

The app checks this repository for new versions (at most every few hours; it can be turned off in Settings) and verifies every download against the `.sha256` file before installing it. It sends nothing else anywhere.

Check a download manually in PowerShell:

```powershell
(Get-FileHash .\PCMonitor-Setup-X.Y.Z.exe -Algorithm SHA256).Hash.ToLower()
```

The result must match the contents of the `.sha256` file.
