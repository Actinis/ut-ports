# Actinis Ubuntu Touch ports

Community device ports for **Ubuntu Touch 24.04 (Noble)**.
Only the 24.04 release line is currently planned for support.

## Repositories

| Repository | Purpose |
| --- | --- |
| [ut-device-sony-pdx213](https://github.com/Actinis/ut-device-sony-pdx213) | Sony Xperia 10 III device adaptation and build configuration |
| [ut-kernel-sony-msm](https://github.com/Actinis/ut-kernel-sony-msm) | Sony MSM kernel sources adapted for Ubuntu Touch |

## Status

Repository infrastructure is being prepared. The Sony port is under active development; source import is pending completion of the current fixes. No public installable release, OTA channel or UBports Installer integration is provided here yet.

Future device ports should have their own `ut-device-<vendor>-<codename>` repository. Kernel repositories use the `ut-kernel-` prefix and may be shared by compatible devices.

Published releases should record exact device and kernel commits, rootfs and Halium builds, toolchain versions and artifact checksums. Hardware support must be documented for each device and release; an OS update channel alone does not establish device readiness.

This is an Actinis community project, not an official UBports release.
