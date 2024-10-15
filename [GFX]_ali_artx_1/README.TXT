ArtX, Inc.
SOFTWARE
USER'S GUIDE

=====================================================
= Installing the Operating System and ArtX software =
=====================================================
The hard disk shipped with the system has Win 98 SE, the ArtX drivers, and the ArtX Tools preinstalled.  If you need to install a new system disk, or if you want to install another operating system, then follow these procedures:
1. Install the Operating System on a partitioned, formatted disk using the standard Microsoft procedure for the specific OS.  The embedded VGA hardware will be used as the display device.
2. Install ArtX Drivers
3. Install ArtX Build Tools, DX 7.0 (Win98 only), and any additional software.

The CD that came with the evaluation board has software for Windows 98, the ArtxX drivers, and some tools.  The ArtX drivers for Win 98 are in \ArtX_Drivers\Win98, the ArtX drivers for Windows 2000 are in \ArtX_Drivers\Win2000, and the tools are in \ATools.  

For more details on OS installation, consult the setup instructions in the Windows 98 Resource Kit, the Getting Started with Microsoft Windows 98 Manual, the Microsoft Windows 2000 Preview Guide, or the Microsoft Web site.



========================================================
= Installing ArtX Drivers on Windows 98 Second Edition =
========================================================
At the end of the OS loading procedure, Windows 98 will be installed and running on the machine.  The display adapter will be set to a "Standard PCI Graphics Adapter (VGA)" running in 16 colors at 640 by 480.  There are two methods for installing ArtX Drivers in Windows 98.

Method #1:
**********
Run the AXINST.EXE from the from D:\ArtX_Drivers\Win98 (where "D:" is the drive letter for the CDROM).

Method #2: Bring up the Display Control Panel and follow these steps:
*********************************************************************
1. Select the "Settings" tab and hit the "Advanced" button. 
2. Select the "Adapter" tab and hit the "Change" button.  This will bring up the "Update Device Driver Wizard."  
3. Hit "Next" and select "Display a list of all the drivers in a specific location, so you can select the driver you want" and hit "Next".  
4. Hit the "Have Disk" button and copy from D:\ArtX_Drivers\Win98 (where "D:" is the drive letter for the CDROM).  
5. Select artx.inf and hit "OK".  The "Select Device" popup will appear with "ArtX Display Device" selected.  
6. Hit "OK", then "Next" and finally "finish".  This will install the display drivers.  Close the control panel applet but don't restart yet.

The GART miniport needs to be installed for AGP accesses.  Follow these steps to install the driver:
----------------------------------------------------------------------------------------------------
1. Bring up the system control panel and select the "Device Manager" tab.
2. Under the "System Devices" entry, double click the "PCI Standard Host CPU Bridge". 
3. Select the "Driver" tab and hit "Update Driver."  This will bring up the "Update Device Driver Wizard". 
4. Hit "Next" and select "Display a list of all the drivers in a specific location, so you can select the driver you want." 
5. Select "Other Devices" and hit "Next".
6. Hit the "Have Disk" button and type D:\ArtX_Drivers\Win98 (where "D:" is the drive letter for the CDROM) into the "Copy Manufacturer's files from:" text box and hit "OK". 
7. Select the "ArtX1 AGP System Controller [date]" and hit "Next" then "Next".  This will install the ArtX GART driver.  Hit "Finish" to complete installation.

One more driver needs to be installed for the ArtX system.  Follow these steps:
-------------------------------------------------------------------------------
1. Bring up the system control panel and select the "Device Manager" tab.  
2. Under the "Other Devices" entry, double click the "PCI Multimedia Video Device".  
3. Select the "Driver" tab and hit "Update Driver."  This will bring up the "Update Device Driver Wizard".  
4. Hit "Next" and select "Display a list of all the drivers in a specific location, so you can select the driver you want." 
5. Select "Other Devices" and hit "Next".
6. Hit the "Have Disk" button and type D:\ArtX_Drivers\Win98 (where "D:" is the drive letter for the CDROM) into the "Copy Manufacturer's files from:" text box.  
7. Install the "ArtX Device [date]".  This will install the special ArtX driver.  

Now restart the computer.  When the system reboots, start the display control panel and set the display to 1024 by 768 in high color (16 bit) mode.
Installing Microsoft DX 7.0 on Windows 98 SE
DirectX 7 is required for the ArtX drivers to function properly.  The DirectX 7 runtime files are located on this CD in the \Directx directory.  The DirectX 7 files can also be downloaded from: DX7.0 Run Time - http://www.microsoft.com/directx/developer/downloads/default.asp



=====================================================
= Installing ALi Bus Master Driver on Windows 98 SE =
=====================================================
Run setup.exe from the \ALI_UDMA directory and follow instructions

To verify that you are using DMA transfer mode for each of the devices you can check your settings by following the steps outlined below.

Select System in Control Panel
Select Device Manager tab
Expand CD-ROM
	Select Property button
	Select Settings tab
	Check DMA checkbox
	Repeat above steps for any other device under CD-ROM if exist
Expand Disk Drives
	Repeat above steps for all hard disks under Disk Drives (ignore the floppy disk)


===========================================
= Installing ArtX Drivers on Windows 2000 =
===========================================
There are two methods for installing ArtX Drivers in Windows 2000.

Method #1:
**********
Run the AXINST.EXE from the from D:\ArtX_Drivers\Win98 (where "D:" is the drive letter for the CDROM).

Method #2: Bring up the Display Control Panel and follow these steps:
*********************************************************************
At the end of the OS loading procedure, Windows 2000 will be installed and running on the machine.  The display adapter uses the standard VGA running in 16 colors at 640 by 480.  To install the Windows 2000 ArtX driver follow these steps:
1. Make sure you are logged into Windows 2000 with Administrator privileges.
2. In the \WINNT\INF directory, delete all of the OEM*.INF and OEM*.PNF files.
3. Bring up the System Control Panel
4. Select the "Hardware" tab and click the "Device Manager" button.
5. Under the "Display adapters" right click on "ArtX1 Device" and select "Uninstall".  When prompted to reboot the machine click "No".
6. Under the "Display adapters" right click on "ArtX1 Display Device" and select "Uninstall".
7. You must now reboot Windows 2000.
8. When the system reboots Plug-n-Play will detect the devices automatically.  Windows will first detect the Multimedia Video Controller.  Click next to advance the "Found New Hardware Wizard".
9. In the next window select "Search for a suitable driver for my device (recommended)" and click "Next".
10. Select "Specify a location" and click "Next".
11. In the "Copy manufacturer's files from:" select D:\ArtX_Drivers\Win2000 (where "D:" is the drive letter for the CDROM) and click "OK".
12. The "Driver Files Search Results" window will indicate "Windows found a driver for this device."  Click "Next" to install the driver.
13. Click "Yes" in the "Digital Signature Not Found" window.
14. Click "Finish".
15. The Video Display Device will be found next. 
16. Click "Yes" in the "Digital Signature Not Found" window.
17. You must now reboot the system.  You will not be prompted to reboot.



===========================================
= Installing ArtX Drivers on Windows NT 4 =
===========================================
1. Make sure you are logged into Windows NT 4 with Administrator privileges.
2. Bring up the System Control Panel.
3. Open the Display Control Panel.
4. Click the settings tab and then click the "Display Type" button.
5. Click the "Change" button.  This will bring up the "Change Display" window.
6. Click the "Have Disk" button and copy from D:\ArtX_Drivers\WinNT (where "D:" is the drive letter for the CDROM). If you are installing the drivers from the self-extracting file, select the directory to which you extracted the driver files (c:\artx by default).
7. Select artxnt4.inf and click "OK".  The "Select Device" popup will appear with "ArtX, Inc. ArtX1" selected.
8. Click "OK", then "Yes" and finally "OK".  This will install the display drivers.  Close the control panel applet and reboot the system.



=========================
= Installing ArtX Tools =
=========================
There are two methods for installing ArtX ATools.

Method #1:
**********
Run the SETUP.EXE from the from D:\ATools (where "D:" is the drive letter for the CDROM).

Method #2:
*********************************************************************
Bring up Windows explorer and copy the \ATools directory on the CDROM to your local hard drive.  The files include some OpenGL demos along with some ArtX specific tools.



====================================
= Software Preinstalled on Systems =
====================================
The hard disk shipped with the system has Windows 98 SE, the ArtX drivers, and the 
ArtX Tools preinstalled.  There is additional software preinstalled on the system.  The additional software includes Ziff Davis WinBench benchmarks, and some other games and test programs.  The Win 98 SE cabinet files have been copied to \win98.

If you do not have cdroms for WinBench, the images can be obtained from 
http://www.zdnet.com/zdbop



===========
= SoloBug =
===========
Solobug is included in this distribution CD in the \SoloBug directory.
Please use this application to report all bugs back to ArtX and complete all relevant fields in the bug report. You may email the SoloBug (*.SBG) file back to your Field Application Engineer or alternately you may email the bug report to support@artxinc.com

ArtX Confidetial

