# 🔴 USE AT YOUR OWN RISK

> [!CAUTION]
> **Recovery may erase data or cause loss/changes of the original serial number (SN) and MAC addresses.**
>
> X110 is Wi-Fi-only. Wi-Fi and Bluetooth do not rely on IMEI, but cannot be guaranteed after NV data damage.
>
> **SM-X110 ONLY — BIT 6 / U6. No other model or revision.**
>
> EXPERIMENTAL — NOT TESTED ON HARDWARE. SUCCESS IS NOT GUARANTEED.

## Quick guide

1. Download the experimental ZIP from Releases and extract the entire archive.

2. Install needed VC++ and USB drivers from 03_DRIVERS. For the MTK driver, right-click INSTALOVAT_MTK.cmd → Run as administrator.

3. Run 02_SP_FLASH_TOOL/SPFlashToolV6.exe.

4. Download-XML: select 01_SPFT_RECOVERY/download_agent/flash.xml. Authentication File: select auth_sv5.auth in that same folder.

5. Choose Download Only. Check that 16 rows are selected and Location paths are populated. Do not change other options.

6. Click Download and connect the tablet by USB. If it is not detected, hold Power + Volume Down until vibration, then release. Do not unplug during writing.

7. After Download OK, unplug USB. To enter Download Mode, hold both volume buttons and reconnect USB; confirm any prompt with a short Volume Up press.

**STOP on any error; do not repeat the same write. If Download Mode does not appear, do not start another write.**

Once Download Mode returns, you can flash matching full official SM-X110 BIT 6 firmware with Odin. Full firmware is not included in this small package.

[Technical details and driver troubleshooting](TECHNICAL_NOTES_EN.md)
