# [GFX]_via_cn700_unichrome_pro

**VIA/S3G UniChrome Pro IGP Display Driver**  
**Version:** 4.14.10.0068 (internal 16.01.23.24)  
**DriverVer:** 08/28/2006  
**Original package:** VIA/S3G UniChrome Family Win9x/ME  
**Target OS:** Windows 98 Second Edition  
**Driver model:** VxD (Miniport) + DLLs  
**Core driver files:** vtdisp.drv, vtmini.vxd  

### Description
Clean package with VIA/S3G UniChrome Pro IGP video driver files from the official 16.01.23.24 distribution.  
Win9x/ME compatible files only. No InstallShield, no NT/2K/XP extras.  
Includes full S3 utilities (Display, Gamma, Overlay, Info, Tray).  
Designed for manual installation or Win98 QuickInstall (DRIVER.EX).

### Supported Hardware
- Northbridge: VIA CN700 / P4M800 Pro / P4M800 CE / VN800  
- IGP: S3 UniChrome Pro (rev 01)  
- Compatible southbridge examples: VIA VT8237  
- **PCI Hardware ID:**  
  `PCI\VEN_1106&DEV_3344`  

### Notes
- VxD driver – supports up to 1920x1440@32bit; requires DirectX 7+ (DX8.1 recommended for overlays/3D).  
- No DOS/3D acceleration included (use VBEMP fallback for basic modes if needed).  
- Auxiliary DLLs/CFGs handle utilities and languages (English, Chinese, Japanese, Korean).  
- Tested on: HP t5530 Thin Client (CN700 rev 01 + VT8237) – works well for basic desktop; also VIA EPIA-M and similar mobos.

### Included Files
- hg202.inf       (main INF)  
- vtdisp.drv      (display driver)  
- vtmini.vxd      (miniport VxD)  
- vtdd.dll        (DirectDraw)  
- vticd.dll       (ICD OpenGL)  
- GTF.dll         (GTF support)  
- VTDisply.dll    (S3Display utility)  
- VTGamma2.dll    (S3Gamma2 utility)  
- VTInfo2.dll     (S3Info2 utility)  
- VTOvrlay.dll    (S3Overlay utility)  
- .cfg files      (configurations for utilities)  
- .hlp files      (help files, multilingual)  
- VTTrayP.exe     (S3TrayPlus)  
- VTTimer.exe     (timer utility)  
- VTUninst.exe    (uninstaller)

Source: Official VIA/S3G UniChrome Pro Win9x package, extracted for retro driver collection.