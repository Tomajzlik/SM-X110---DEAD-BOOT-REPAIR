# SM-X110 U6 / BIT 6 — untested Download Mode recovery candidate

**EXPERIMENTAL. NOT HARDWARE-TESTED. NO GUARANTEE OF BOOT OR DOWNLOAD MODE RECOVERY. SM-X110 ONLY, ANDROID 15 X110XXS6CYI3, BIT 6. NOT X115, BIT 7/9 OR A16.**

This reduced profile was derived from the user-supplied X110XXS6CYI3 INS service set. The user's earlier successful X110 repair involved the full original set, not this reduced selection. Images are unchanged. Addresses come from the supplied UFS layout and have not been checked against your tablet's GPT.

Selected images: spmfw, dpm1, scp1, sspm1, mcupm1, gz1, lk1, tee1, dtbo, vbmeta, tzar, pi_img, boot, recovery, vendor_boot and vbmeta_system. BOOT_ONLY_CONTENTS.json lists exact addresses and sizes. Kernel/recovery images form part of this boot set; it is not a complete Android installation. Its intended purpose is recovering access to Download Mode, not installing a fully working OS.

Preloader, GPT/PIT, super, userdata, efuse, grd_fw, NV/EFS/persist and donor identity files are excluded and not selected for writing. Missing efs.img, sec_efs.img, persist.img and vbmeta_vendor.img references in the original XML are disabled, not substituted. This profile cannot repair a damaged preloader. Other missing or incompatible boot components may also prevent recovery.

Before writing, use Read Back to save your boot areas and NV/EFS, and compare actual GPT addresses. Stop on any mismatch. Recovery can cause data loss or invalid/changed serial number and MAC addresses; original identity cannot be guaranteed without your own backups. X110 is a Wi-Fi model, not an LTE model with normal cellular calls/IMEI. This package cannot restore factory identity.

Extract the entire ZIP to a short local path such as D:/X110_RECOVERY. Run 02_SP_FLASH_TOOL/SPFlashToolV6.exe. Download-XML: 01_SPFT_RECOVERY/download_agent/flash.xml. Authentication: 01_SPFT_RECOVERY/download_agent/auth_sv5.auth. Use Download Only with 16 selected existing files and populated Location fields. Never use Format All, Firmware Upgrade, Nand Erase or add preloader/efuse/NV writes. Write only after GPT verification. Stop on signature/layout errors; earlier partitions may already have been written. Download OK is not proof of boot. Once Download Mode works, use matching full official SM-X110 BIT 6 firmware in Odin; that firmware is included in 05_OFFICIAL_A15.

The included signed MediaTek cdc-acm.inf driver is old and may be blocked by Windows Memory integrity. Prefer a compatible vendor driver. Installation requires administrator rights. If Memory integrity is manually disabled temporarily for repair, remove the driver and re-enable protection afterwards. Do not disable Defender, Secure Boot or signature enforcement. VC++ x86/x64 and Samsung USB installers are in 03_DRIVERS; install only when needed.


Complete kit: official Samsung FUS INS Android 15 BIT 6, X110XXS6CYI3 / X110ODM6CYI3. All four Odin TAR.MD5 checks passed. All 16 recovery image SHA-256 hashes match the corresponding decompressed official BL/AP images. Existing 16-image UFS profile is unchanged. No hardware test has been performed. Full firmware is supplied separately for Odin; SP Flash Tool does not write super, userdata, preloader, GPT, efuse or NV/EFS. X110 is Wi-Fi-only: no CP file.
