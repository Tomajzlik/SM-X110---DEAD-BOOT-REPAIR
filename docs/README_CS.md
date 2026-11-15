# SM-X110 U6 / BIT 6 — neovereny kandidat obnovy Download Mode

**EXPERIMENTALNI. NEOTESTOVANO NA TABLETU. ZADNA ZARUKA STARTU ANI OBNOVY DOWNLOAD MODE. POUZE SM-X110, ANDROID 15 X110XXS6CYI3, BIT 6. NE X115, NE BIT 7/9, NE A16.**

Tento zmenseny profil vznikl z uzivatelem dodane sady X110XXS6CYI3 INS. Jeho uspech neni dolozen testem: predchozi zprava o opravenem X110 se tyka cele puvodni sady, nikoli tohoto vyberu. Obrazy nebyly upravovany; adresy pochazeji z dodane UFS sekce a nejsou overene proti GPT vaseho konkretniho tabletu.

Vybrano je 16 obrazu: spmfw, dpm1, scp1, sspm1, mcupm1, gz1, lk1, tee1, dtbo, vbmeta, tzar, pi_img, boot, recovery, vendor_boot, vbmeta_system. BOOT_ONLY_CONTENTS.json uvadi presne adresy a velikosti. Kernel/recovery obrazy jsou zahrnuty jako soucast bootovaci sady, nikoli jako cely Android. Cilem je vratit pristup k Download Mode; profil nema nainstalovat kompletni funkcni Android.

Balicek NEOBSAHUJE a NEZAPISUJE preloader, GPT/PIT, super, userdata, efuse, grd_fw, EFS/sec_efs/NVRAM/NVDATA/persist ani donorove identity. Odkazy na chybejici efs.img, sec_efs.img, persist.img a vbmeta_vendor.img z puvodniho XML jsou vypnute a nemaji byt nicim nahrazovany. Pokud je poskozen samotny preloader, tento profil nestaci. Take chybejici nebo nekompatibilni jiny bootovaci oddil muze obnovu znemoznit.

Pred jakymkoliv zapisem si pres Read Back zazalohujte vlastni bootovaci oblasti a NV/EFS a overte skutecnou GPT. Nesoulad adres = STOP. Obnova muze vest ke ztrate dat nebo zmenenemu/neplatnemu SN a MAC adresam; bez vlastni zalohy nelze slibit obnovu puvodni identity. X110 je Wi-Fi model, nikoli LTE model s beznymi hovory/IMEI. Tento archiv identitu neopravuje.

Rozbalte cely ZIP do kratke cesty (napr. D:/X110_RECOVERY). Spustte 02_SP_FLASH_TOOL/SPFlashToolV6.exe. Download-XML: 01_SPFT_RECOVERY/download_agent/flash.xml. Authentication: 01_SPFT_RECOVERY/download_agent/auth_sv5.auth. V Download Only musi byt vybrano 16 existujicich souboru a vyplnene Location. Nikdy Format All, Firmware Upgrade, Nand Erase nebo rucni pridavani preloaderu/efuse/NV. Zapis az po overeni GPT; pri chybe podpisu nebo rozlozeni neopakovat naslepo, protoze predchozi oddily uz mohou byt zapsane. Download OK neni dukaz funkcniho bootu. Po obnove Download Mode pouzijte odpovidajici kompletni oficialni firmware SM-X110 BIT 6 v Odinu; ten zde neni zahrnut.

Prilozeny MediaTek ovladac cdc-acm.inf je stary podepsany ovladac a Windows jej muze blokovat kvuli Integrite pameti. Prednost ma kompatibilni ovladac od vyrobce. Instalace vyzaduje administratora. Je-li pro opravu rucne docasne vypnuta Integrita pameti, po odstraneni ovladace ji znovu zapnete. Nevypinejte Defender, Secure Boot nebo kontrolu podpisu. VC++ x86/x64 a Samsung USB instalatory jsou ve 03_DRIVERS; instalaci provedte jen pokud je potrebujete.
