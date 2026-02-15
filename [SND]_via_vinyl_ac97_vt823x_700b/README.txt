# [SND]_via_vinyl_ac97_vt823x_700b

**VIA Vinyl AC'97 Codec Combo WDM Driver**  
**Version:** 6.14.01.4200  
**DriverVer:** 06/27/2007  
**Original package:** VIA Vinyl v7.00b  
**Target OS:** Windows 98 Second Edition  
**Driver model:** WDM (Kernel Mode)  
**Core driver file:** vinyl97.sys  

### Description
Clean package with VIA Vinyl AC'97 audio driver files from the official v7.00b distribution.  
Win9x/ME compatible files only. No installer, no ADeck control panel, no NT/2K/XP extras.  
Designed for manual installation or Win98 QuickInstall (DRIVER.EX).

### Supported Hardware
- Southbridge: VIA VT823x series (AC'97 Audio Controller)  
  - VT8233 / VT8233A / VT8233C  
  - VT8235 / VT8235M / VT8235CE  
  - VT8237 / VT8237R / VT8237A (rev 06, rev 60 included)  
- Compatible northbridge examples: VIA CN700 / P4M800 / VN800  
- **PCI Hardware ID:**  
  `PCI\VEN_1106&DEV_3059`  

### Notes
- WDM driver – requires DirectX 8.0+ (DX 8.1 or 9.0c recommended for full features).  
- No legacy VxD/SBPro DOS support included (use older VIA packages for DOS emulation if needed).  
- Auxiliary INF files (Vinyl971.inf, Vinyl972.inf, VinylCmp.inf) handle codec variants (VT1612/1616/1618).  
- Tested on: HP t5530 Thin Client (VT8237 rev 60 + CN700) – works perfectly without tweaks; also VIA EPIA boards and Shuttle VT8237 systems.

### Included Files
- Vinyl97.inf     (main INF)  
- Vinyl971.inf    (auxiliary codec)  
- Vinyl972.inf    (auxiliary codec)  
- VinylCmp.inf    (combo/auxiliary)  
- vinyl97.sys     (WDM kernel driver)  
- vinyl97.cat     (WHQL catalog, referenced in INF)

Source: Official VIA Vinyl AC'97 v7.00b Win9x package, extracted for retro driver collection.