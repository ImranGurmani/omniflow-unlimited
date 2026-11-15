# Release Status — v1.3.0 (LOCAL DRAFT, NOT PUBLISHED)

**Verdict: the customer release is HELD as a local draft.** No installer has been
published, and no nonfunctional installer will be published. This file records the exact
gates and the current blocker, evidence-based. Nothing here claims unverified
functionality as working.

## Why it is held

The current installer (`OmniFlow_Setup_v1.3.0.exe`, RC build) is **not customer-ready**:

1. **Licensing URL is a local placeholder.** `licensingApiBase = http://127.0.0.1:4100/api/v1`.
   Customers cannot activate against a live service. The installer must be rebuilt with
   the production HTTPS URL.
2. **No live portal is deployed.** Hostinger account access, a confirmed domain, and
   Supabase credentials were not available, so the licensing portal is prepared but not
   live. **No deployment success is claimed.**
3. **Real generation is UNVERIFIED.** Automated tests use synthetic data/mocks; real
   Flow/Muse generation requires the customer's own authorized accounts and has not been
   exercised end-to-end.
4. **Unsigned installer.** No code-signing certificate; SmartScreen will warn.

## Gates that must ALL pass before publishing

- [ ] Production licensing portal deployed and reachable over **HTTPS** (`/healthz` OK).
- [ ] Installer **rebuilt** with `--api-base=<live HTTPS URL>` (placeholder removed).
- [ ] Embedded public verification key **matches** the active production signing key.
- [ ] Mandatory launch checks pass: **activation** + **authorized real generation**.
- [ ] **Clean-Windows** install/activation verification (isolated smoke tests are not a
      substitute).
- [ ] Final SHA-256 checksums regenerated and published with the approved asset.

Only then: attach the installer as a **GitHub Release asset**, publish the release, and
push the `v1.3.0` tag. The installer is never committed to ordinary Git history.

## Exact owner actions (in order)

1. Provide Hostinger access (hPanel or VPS SSH) and confirm the domain + DNS.
2. Create a Supabase PostgreSQL project; copy its connection string (`DATABASE_URL`).
3. Securely transfer the matching production signing **private** key to the host's
   `SECRETS_DIR/keys/` (never via Git, never printed).
4. Deploy the portal from the private repo
   (`omniflow-license-portal`, `docs/DEPLOY_HOSTINGER.md`): `npm ci --omit=dev` →
   `npm run bootstrap:prod` → `npm start`; verify `GET /healthz`.
5. Rebuild the desktop app + installer with the live `--api-base`; verify the key match.
6. Run the launch checks (activation + authorized real generation) and a clean-Windows test.
7. Publish: attach the approved installer as a Release asset, regenerate checksums,
   publish the release, push tag `v1.3.0`.

## Current build fingerprints (RC, not for distribution)

See [`../../CHECKSUMS_SHA256.txt`](../../CHECKSUMS_SHA256.txt). These will be replaced by
the final approved installer's checksums at publish time.