# OmniFlow Studio v1.3.0 — Release Notes (DRAFT)

> **Status: DRAFT — not published.** This release is prepared but held until the
> production gates pass. No installer is attached yet. See
> [`RELEASE_STATUS.md`](RELEASE_STATUS.md).

## Highlights

- **Server-authoritative OMNI2 licensing** with Ed25519-signed entitlements, device
  binding, and an offline grace window.
- **Per-user installer** that preserves your generated videos and settings across
  upgrades and uninstall.
- **Self-contained launcher** — no separate .NET installation needed.
- Generation through **your own** logged-in Google Chrome sessions (Google Flow and
  Muse.ai). Your accounts and credits stay yours.

## Requirements

Windows 10/11 x64, WebView2 Evergreen Runtime, and Google Chrome signed in to your own
Flow/Muse accounts. See [`../../SYSTEM_REQUIREMENTS.md`](../../SYSTEM_REQUIREMENTS.md).

## Installation

See [`../../INSTALL.md`](../../INSTALL.md). The approved installer will be attached to
this release as a GitHub Release asset once published.

## Checksums (current RC build — not for distribution)

The final approved installer will be rebuilt against the live licensing service and its
checksums published here. Current pre-release build fingerprints are tracked in
[`../../CHECKSUMS_SHA256.txt`](../../CHECKSUMS_SHA256.txt).

## Known limitations

- Unsigned installer (SmartScreen warning expected). Verify the checksum and use only
  official Release assets.
- Real generation requires your own authorized accounts and an activated license.