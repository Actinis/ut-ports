# Actinis Ubuntu Touch ports

Community device ports for **Ubuntu Touch 24.04 (Noble)**.
Only the 24.04 release line is currently planned for support.

## Repositories

| Repository | Purpose |
| --- | --- |
| [ut-device-sony-pdx213](https://github.com/Actinis/ut-device-sony-pdx213) | Sony Xperia 10 III device adaptation and build configuration |
| [ut-kernel-sony-msm](https://github.com/Actinis/ut-kernel-sony-msm) | Sony MSM kernel sources adapted for Ubuntu Touch |

## Status

Sony Xperia 10 III sources are published as an experimental community port for XQ-BT52. The device repository contains the locked Noble adaptation and full image assembly workflow; the buildable kernel branch is `main`, with full upstream history and in-tree AppArmor/PMF changes. CI uses a published, checksum-pinned vendor input with a pinned build report and assembles boot, DTBO, userdata and vbmeta candidates. Sony OEM must be obtained separately by the device owner. Publication of the vendor input was authorized by the maintainer; the Sony audio-calibration licensing clarification remains unresolved. Stock-baseline installation/restoration and remaining hardware qualification still gate an installation release. Kernel/boot development prereleases and CI candidate artifacts are available; no installation release, OTA channel or universal UBports Installer integration is provided.

Future device ports should have their own `ut-device-<vendor>-<codename>` repository. Kernel repositories use the `ut-kernel-` prefix and may be shared by compatible devices.

Published releases should record exact device and kernel commits, rootfs and Halium builds, toolchain versions and artifact checksums. Hardware support must be documented for each device and release; an OS update channel alone does not establish device readiness.

This is an Actinis community project, not an official UBports release.


## Local workspace contract

Checkouts: `ut-ports`, `ut-device-sony-pdx213`, `ut-kernel-sony-msm`.
Set `UT_PORTS_DATA_DIR` to a separate data volume and explicitly supply compiler
and source paths. Data directories are `downloads/`, `toolchains/`,
`builds/pdx213/<build-id>/`, `releases/pdx213/<tag>/`,
`evidence/pdx213/<test-id>/`, and `private/pdx213/`.
Private data must never be committed or attached to a release.

The [device build instructions](https://github.com/Actinis/ut-device-sony-pdx213/blob/main/docs/BUILD.md)
and [input contract](https://github.com/Actinis/ut-device-sony-pdx213/blob/main/docs/SOURCES.md)
separate verified CI image assembly, owner-supplied Sony OEM and actual
phone qualification. Only the current Noble adaptation is supported.
