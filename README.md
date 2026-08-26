# cc-switch fork build controller

This default branch only hosts the manual GitHub Actions build workflow for this fork. Application source is kept on release-specific branches.

## Branch convention

Each patched branch is based on the matching upstream release tag and contains the local proxy schema fix:

- `codex/v3.19.2-local-fix`
- `codex/v3.20.0-local-fix`
- Future releases: `codex/vX.Y.Z-local-fix`

## Build Windows and Linux packages

1. Open **Actions** → **Windows and Linux Build** → **Run workflow**.
2. Choose `fork` to build a patched branch, or `upstream` to build an official release/tag/branch.
3. Enter the desired ref. The default is `codex/v3.20.0-local-fix`.

The workflow produces:

- Windows x86_64: MSI and portable ZIP
- Linux x86_64: AppImage, DEB, and RPM

Artifacts are retained for 14 days.

Upstream repository: <https://github.com/farion1231/cc-switch>
