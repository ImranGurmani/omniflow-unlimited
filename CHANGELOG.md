# Changelog

All notable customer-facing changes to OmniFlow Studio.

## [1.3.0] — release in preparation

Rebuilt from the 1.2.0 application with a new server-authoritative licensing platform.

### Added
- **OMNI2 licensing**: server-authoritative activation with Ed25519-signed entitlements,
  device binding, and an offline grace window.
- **Per-user installer** (`%LOCALAPPDATA%\OmniFlow`) that preserves generated videos and
  settings across upgrades and uninstall.
- **Self-contained launcher** — no separate .NET installation required.
- Admin-managed license lifecycle: issuance (monthly / annual / lifetime), renewal,
  revocation, and device transfer.

### Changed
- Generation runs through the customer's own logged-in Google Chrome sessions
  (Google Flow and Muse.ai). Accounts and credits remain the customer's own.

### Known limitations
- Installer is **unsigned** (SmartScreen warning expected).
- The public installer is finalized against the live licensing service before release;
  see [`release/v1.3.0/RELEASE_STATUS.md`](release/v1.3.0/RELEASE_STATUS.md).

## [1.2.0] — baseline

Original production application (multi-account AI video generation desktop tool).