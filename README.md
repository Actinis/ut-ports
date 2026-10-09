# Actinis Ubuntu Touch ports

Community device ports for **Ubuntu Touch 24.04 (Noble)**.
Only the 24.04 release line is currently planned for support.

## Repositories

| Repository | Purpose |
| --- | --- |
| [ut-device-sony-pdx213](https://github.com/Actinis/ut-device-sony-pdx213) | Sony Xperia 10 III device adaptation and build configuration |
| [ut-kernel-sony-msm](https://github.com/Actinis/ut-kernel-sony-msm) | Sony MSM kernel sources adapted for Ubuntu Touch |

## Status

Sony Xperia 10 III sources are published as an experimental community port for XQ-BT52. The device repository contains the locked Noble adaptation and real kernel/boot workflow; the buildable kernel branch is `pdx213-halium11-noble`, with full upstream history and in-tree AppArmor/PMF changes. Manual vendor/OEM provenance, stock-baseline installation/restoration and remaining hardware qualification still gate an installable release. No public image release, OTA channel or universal UBports Installer integration is provided.

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
separate reproducible kernel/boot compilation, manual image inputs and actual
phone qualification. Only the current Noble adaptation is supported.
