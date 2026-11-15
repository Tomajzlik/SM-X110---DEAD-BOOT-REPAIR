# 🔴 NA VLASTNÍ RIZIKO

> [!CAUTION]
> **Obnova může způsobit ztrátu dat nebo ztrátu/změnu původního SN a MAC adres.**
>
> X110 je Wi-Fi model. Wi-Fi a Bluetooth nejsou závislé na IMEI, jejich funkčnost po poškození NV dat ale nelze zaručit.
>
> **POUZE SM-X110 — BIT 6 / U6. Ne pro jiný model nebo revizi.**
>
> EXPERIMENTÁLNÍ — NEOTESTOVÁNO NA TABLETU. ÚSPĚCH NENÍ ZARUČEN.

## Stručný návod

1. Stáhni všechny díly .zip.001 až .zip.004 do stejné složky. V 7-Zip otevři .zip.001 a celý balíček rozbal.

2. Ve složce 03_DRIVERS nainstaluj potřebné VC++ a USB ovladače. MTK ovladač: klikni pravým na INSTALOVAT_MTK.cmd → Spustit jako správce.

3. Spusť 02_SP_FLASH_TOOL/SPFlashToolV6.exe.

4. Download-XML: vyber 01_SPFT_RECOVERY/download_agent/flash.xml. Authentication File: vyber auth_sv5.auth ze stejné složky.

5. Zvol Download Only. Musí být zaškrtnuto 16 položek a vyplněné cesty Location. Jiné volby neměň.

6. Klikni Download a připoj tablet k USB. Když se nepřipojí, drž zapínání + hlasitost dolů do vibrace a potom pusť. Během zápisu kabel neodpojuj.

7. Po Download OK odpoj USB. Pro Download Mode drž obě hlasitosti a znovu připoj USB; případnou výzvu potvrď krátce hlasitostí nahoru.

**Při jakékoli chybě STOP — stejný zápis neopakuj. Když se Download Mode neobjeví, další zápis nespouštěj.**

Po návratu Download Mode rozbal ZIP z 05_OFFICIAL_A15. Spusť Odin z 04_ODIN, přiřaď BL → BL, AP → AP a CSC → CSC (ne HOME_CSC). CP nech prázdné. Re-Partition a Nand Erase musí být vypnuté, PIT prázdné. Klikni Start a počkej na PASS. Tato obnova smaže uživatelská data.

[Technické podrobnosti a problémy s ovladači](TECHNICAL_NOTES_CS.md)
