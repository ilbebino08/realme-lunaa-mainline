# Realme GT Master Edition (lunaa) — experimental mainline kernel builds

Build automation for the **experimental**, unofficial mainline Linux port for the Realme GT Master Edition (RMX3360/61/63).

Upstream work belongs to [theleafir1](https://github.com/theleafir1):
- [Kernel fork](https://github.com/theleafir1/linux/tree/sc7280-7.2.y)
- [pmaports fork](https://github.com/theleafir1/pmaports)

## Build

Open **Actions → Build Realme lunaa mainline kernel → Run workflow**.

The workflow uses a native GitHub-hosted ARM64 runner, checks the device-tree source, works around the `.gitignore` / `rsync --exclude-from` issue affecting `kernel/time/timeconst.bc`, and attempts to build the `linux-postmarketos-qcom-sc7280` package using pmbootstrap.

If successful, download **realme-lunaa-kernel-apk** from the workflow's Artifacts section.

This workflow is an initial experimental implementation: the first run may uncover dependency, initialization, disk-space or toolchain issues. Inspect the Actions logs and adjust accordingly.

## Safety

**Do not flash this package or an image built from it directly.** A successful compilation does not prove the firmware boots, that the DTB is correct, or that the device can be recovered. The workflow does not unlock devices or flash partitions.

This project is not affiliated with Realme, Nura, or the original maintainer.
