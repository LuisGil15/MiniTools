# MiniTools Distribution

Private release channel for MiniTools while signing, notarization, and update
delivery are being finalized.

## Release contract

Each GitHub release should use a semantic version tag such as `v1.1.0` and
include:

- `MiniTools.zip` — signed and notarized application bundle.
- `MiniTools.zip.sha256` — SHA-256 checksum for the archive.
- `latest.json` — release metadata consumed by MiniTools.

`latest.json` is committed as a safe empty template. The release workflow will
replace its nullable fields only after the archive has been signed, notarized,
uploaded, and verified.

## Safety rules

- Never publish an unsigned production archive.
- Never reuse a version or build number.
- Verify the checksum after downloading the uploaded asset.
- Keep the repository private until the public release channel is approved.
