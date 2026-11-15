# System Requirements

## Minimum

| Component | Requirement |
| --- | --- |
| OS | Windows 10 (64-bit) or Windows 11 |
| Architecture | x64 |
| RAM | 8 GB (16 GB recommended for video generation) |
| Disk | ~500 MB for the app, plus space for generated videos |
| Runtime | Microsoft Edge **WebView2 Evergreen Runtime** |
| Browser | **Google Chrome** (latest), signed in to your own accounts |
| Network | Internet connection for license activation and generation |

## Notes

- **No .NET prerequisite.** The launcher ships self-contained (.NET bundled, win-x64).
- **WebView2** is preinstalled on most Windows 11 systems. If missing, install the
  Evergreen Bootstrapper from Microsoft.
- **Google Chrome is required for generation.** OmniFlow drives Google Flow and Muse.ai
  through your own logged-in Chrome sessions. You must have your own authorized accounts
  and any required credits/entitlements on those services.
- **Per-user install.** The app installs to `%LOCALAPPDATA%\OmniFlow` and does not require
  administrator rights.
- **Unsigned installer.** There is no code-signing certificate yet; Windows SmartScreen
  will warn. Verify the SHA-256 checksum and only use official Release assets.

## Licensing

- An activated **OMNI2** license key is required for generation.
- Activation binds the license to the device; an offline grace window allows continued
  use if the licensing service is briefly unreachable.