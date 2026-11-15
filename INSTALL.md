# Installing OmniFlow Studio

> The public installer is published as a **GitHub Release asset** once the production
> release gates pass. Until then there is no customer download. See
> [`release/v1.3.0/RELEASE_STATUS.md`](release/v1.3.0/RELEASE_STATUS.md).

## 1. Check prerequisites

See [`SYSTEM_REQUIREMENTS.md`](SYSTEM_REQUIREMENTS.md). In short:

- Windows 10 or 11, 64-bit.
- **Microsoft Edge WebView2 Evergreen Runtime** (usually preinstalled on Windows 11).
- **Google Chrome**, signed in to your own Google Flow and Muse.ai accounts.

The launcher is self-contained (.NET bundled) — you do **not** need to install .NET.

## 2. Download and verify

1. Download `OmniFlow_Setup_v1.3.0.exe` from the official
   [Releases page](https://github.com/ImranGurmani/omniflow-unlimited/releases).
2. Verify the SHA-256 checksum against [`CHECKSUMS_SHA256.txt`](CHECKSUMS_SHA256.txt):

   ```powershell
   Get-FileHash .\OmniFlow_Setup_v1.3.0.exe -Algorithm SHA256
   ```

   Only run the installer if the hash matches. Do not use builds from anywhere else.

## 3. Install

1. Run `OmniFlow_Setup_v1.3.0.exe`.
2. Windows SmartScreen may warn because the installer is **unsigned**. Confirm the
   publisher/source is the official Releases page and the checksum matches before
   proceeding. Never bypass SmartScreen for an unverified file.
3. The app installs per-user to `%LOCALAPPDATA%\OmniFlow`. No administrator rights are
   required.

Your generated videos and settings are preserved across upgrades and uninstall.

## 4. Activate your license

1. Launch OmniFlow.
2. Enter your **OMNI2** license key when prompted.
3. The app activates online and binds to this device. Generation is enabled while the
   license is active.

If activation fails, check your internet connection and that the key is valid, then see
[`SUPPORT.md`](SUPPORT.md).

## 5. Uninstall

Use Windows **Settings → Apps → OmniFlow → Uninstall**. Your user data folder is left in
place so a reinstall keeps your videos and settings.