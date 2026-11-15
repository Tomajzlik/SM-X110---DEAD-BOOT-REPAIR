# Samsung SM-X110 — BIT 6 / U6 only

**Never use this package for another model, BIT 7/9, or an unverified Android 16 downgrade.**

[Česky](docs/README_CS.md) · [English](docs/README_EN.md) · [Русский](docs/README_RU.md)

## EXPERIMENTAL — not tested on hardware

This is a **new reduced candidate** intended to recover access to Download Mode. It is not a proven repair, not a complete OS, and has **no 100% success guarantee**. The user-reported earlier successful X110 repair involved the full original set, not this reduced profile.

Source: user-supplied X110XXS6CYI3 INS Android 15 BIT 6 images. The selected 16 images are unchanged; addresses were taken from the supplied UFS layout. **The actual tablet GPT must be read and checked before any write.**

## Download

[Open the experimental release](https://github.com/Tomajzlik/SM-X110---DEAD-BOOT-REPAIR/releases/tag/v2026.11.15-u6-download-mode-experimental) and download **SM-X110_BIT6_DOWNLOAD_MODE_EXPERIMENTAL.zip** plus **SHA256SUMS.txt**. The ZIP contains the 16 images, DA/auth, relative-path XML, SP Flash Tool V6, drivers/runtime installers and CS/EN/RU guides. Extract the full ZIP to a short path. Do not use GitHub's automatic “Source code” ZIP as a firmware package.

## Scope

Selected: spmfw, dpm1, scp1, sspm1, mcupm1, gz1, lk1, tee1, dtbo, vbmeta, tzar, pi_img, boot, recovery, vendor_boot, vbmeta_system. See [exact contents and addresses](BOOT_ONLY_CONTENTS.json).

Not included/selected: Preloader, GPT/PIT, super, userdata, efuse, grd_fw, NV/EFS/persist or donor identity data. Missing identity/persist/vbmeta_vendor references from the old full XML are disabled, not substituted. A damaged Preloader or other incompatible boot component will not be fixed by this profile.

The [profile XML](profile/scatter.xml) is provided for inspection only; the usable package, images, DA and schema are in the release ZIP. No device-identification dumps or personal backups are published.

## Before writing

Read the matching language guide. Back up your own boot regions and NV/EFS and verify actual GPT, storage type and bootloader revision. Use **Download Only**, never Format All, Firmware Upgrade or Nand Erase. Stop on a signature/layout error; do not retry unchanged because earlier partitions may already have been written. “Download OK” confirms transfer, not successful boot.

Recovery may cause data loss or invalid/changed factory identity (SN, original Wi-Fi/Bluetooth MAC, and IMEI/cellular service on LTE models). This is not proof that the limited profile itself caused identity loss in the original case: NV/EFS was already damaged. These packages do not restore factory identity and contain no donor NV/EFS. SM-X110 is Wi-Fi-only.

Third-party firmware and tools retain their original ownership and terms. These are community recovery archives, not official Samsung repair tools or a manufacturer-supported procedure. See [sources](SOURCES.txt).
