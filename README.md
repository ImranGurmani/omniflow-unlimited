# OmniFlow Studio

**OmniFlow** is a Windows desktop application for AI video generation. It drives
generation through **your own** logged-in browser sessions (Google Flow and Muse.ai),
so your accounts, credits and sessions stay yours. Licensing is server-authoritative:
each install activates an **OMNI2** license key against the OmniFlow licensing service.

- **Current version:** 1.3.0 (base application 1.2.0)
- **Platform:** Windows 10 / 11, 64-bit (x64)
- **Install scope:** per-user (`%LOCALAPPDATA%\OmniFlow`); your generated videos and
  settings are preserved across upgrades and uninstall.

> **Release status: preparation / draft.** The customer installer is being finalized
> against the live licensing service. A public download will appear here only after the
> production release gates pass. See [`release/v1.3.0/RELEASE_STATUS.md`](release/v1.3.0/RELEASE_STATUS.md).

## What's in this repository

This is the **public release** repository. It contains customer-facing documentation and
release metadata only — **not** the application source code:

| File | Purpose |
| --- | --- |
| [`INSTALL.md`](INSTALL.md) | Step-by-step installation |
| [`SYSTEM_REQUIREMENTS.md`](SYSTEM_REQUIREMENTS.md) | OS, runtime and browser prerequisites |
| [`CHANGELOG.md`](CHANGELOG.md) | Version history |
| [`SUPPORT.md`](SUPPORT.md) | How to get help |
| [`CHECKSUMS_SHA256.txt`](CHECKSUMS_SHA256.txt) | SHA-256 fingerprints of release builds |
| [`release/v1.3.0/`](release/v1.3.0/) | Release notes + release status |

Approved installers are published as **GitHub Release assets** (not committed to Git
history). See the [Releases page](https://github.com/ImranGurmani/omniflow-unlimited/releases).

## How licensing works

1. Install OmniFlow and launch it.
2. Enter your **OMNI2** license key (format `OMNI2-XXXXX-XXXXX-…`).
3. The app activates against the licensing service and binds to your device.
4. Generation is enabled while your license is active (with an offline grace window).

You need your own logged-in **Google Flow** and **Muse.ai** sessions in Google Chrome for
generation. OmniFlow does not provide accounts or credits.

## Important notices

- The installer is **unsigned** (no code-signing certificate yet). Windows SmartScreen
  will show a warning. Only install builds published on the official Releases page, and
  verify the SHA-256 checksum. Never bypass SmartScreen for an unverified download.
- Real generation requires your own authorized accounts and an activated license.