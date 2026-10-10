# Release procedure

Only Ubuntu Touch 24.04 (Noble) is currently supported.

## Preparation

1. Import and review the device sources and full kernel history with upstream licenses and provenance.
2. Populate and validate the source lock. Build from a clean checkout using verified inputs.
3. Record the device adaptation commit, kernel commit, workflow run and toolchain version.
4. Qualify the resulting images on the exact device variant. Document failures and untested hardware.
5. Publish a draft release with the manifest, checksums, changelog and reviewed installation/restoration instructions.
6. Review the draft and device results before making it public. Creating a tag alone must not publish a release.

## Naming

Device release tag: `pdx213-noble-port-v0.1.0` (example).
Artifacts: `pdx213-noble-port-v0.1.0-boot.img`, plus other images only when required by the qualified installation method.
Include `SHA256SUMS`, `sources.lock.json`, `release-manifest.json` and hardware qualification notes.

The release manifest records the exact device commit separately from the source lock to avoid a self-referential commit hash. It also records artifact names, sizes and SHA256 values, build provenance and tested device variants. Do not attach personal backups or vendor binaries without confirmed redistribution permission.

The device workflow assembles full Noble candidates on GitHub-hosted runners using the published, checksum-pinned vendor and its build report. These candidates contain boot, DTBO, userdata, vbmeta, checksums and flashing instructions; Sony OEM is excluded and must be obtained separately by the owner. Maintainer authorization to publish the vendor input does not assert a completed licensing review; the Sony audio-calibration clarification remains unresolved. The workflow also publishes kernel/boot development prereleases. It does not flash a phone or publish a full installation release. An initial candidate name is `pdx213-noble-port-v0.1.0-alpha.1`, only after input provenance, stock-baseline installation/restoration and exact-build device qualification are resolved.
