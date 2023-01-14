================================================================================
AU8810 Windows 95 /98 Driver                                          README.TXT
================================================================================

This is version 4.06.3220 of the Aureal Vortex AU8810 driver for Windows 95 and 
Windows 98.


I.  Overview
------------

A.  SYSTEM REQUIREMENTS:

	1. AU8830 sound card with Installation & Driver CD-ROM. 
	2. Access to Microsoft Windows 95 or Microsoft Windows 98 installation 
	   CD-ROM. 
	3. Windows 95/98 PC with:
	  *   100+MHz, >16MB DRAM, >15MB disk space, and CDROM
	      drive
	  *   Available PCI slot.
	4. Good-quality speakers or headphones and connecting cables. 
	5. Joystick and MIDI keyboard for testing the gameport. 

    Wavetable Memory Requirements:
  
      The Vortex hardware wavetable engine uses a native 4MB sample set. The 
      samples are stored on hard disk and swapped to DRAM as required. The 
      typical DRAM footprint is <2MB. As a result, the Vortex sample set 
      provides better sound quality than 2MB sample sets offered by other 
      vendors, but does not require more memory. 


B.  NEW FEATURES:

II.  QUICK START
----------------

	1.  Remove any existing Vortex drivers from previous installations. 
	2.  Install the Vortex hardware.
	3.  Install the Vortex Windows 95/98 drivers, Microsoft DirectX 6.0, 
	    and Vortex demonstration applications.

    In most cases, you will be able to insert the card into your computer, 
    insert the Vortex CD-ROM into the CD-ROM drive, and follow the on-screen 
    prompts for complete system installation. 




III. SOFTWARE INSTALLATION
--------------------------

A. DRIVER INSTALLATION 

   If you have older drivers in your system, please uninstall them first 
   as described in Section C below. 


	1.  Power on the system, placing the "Vortex Installation & Driver Disk"
	    in the CD-ROM drive.
	2.  During the load process, Windows 95/98 should detect the Vortex PCI
	    board and display a message such as "New Hardware Found". If Windows
	    prompts you for the drivers of the "PCI Multimedia Audio Device",
	    then select "Driver Disk Provided by Manufacturer"
	    Select the Vortex CD-ROM's \Win95 directory. 

   Note: Some Windows 95 versions (OSR2) do not show this prompt. Instead, 
   they ask whether to search the diskette and CD-ROM drives for the 
   appropriate drivers.

   Installed drivers may include Vortex PCI audio, Vortex wavetable, Vortex
   mixer, DOS modem port, Vortex gameport interface, Vortex MPU401 interface,
   and Vortex Sound Blaster emulation. 

   Depending on the version of Windows 95 and the configuration of the 
   system, you may be prompted to provide several file locations. Here are 
   the CD-ROMs and directory locations for which you may be prompted:


        Vortex Installation & Driver Disk		\Win95
        Windows 95/98 Installation Disk			\Win95 
        Microsoft DirectX 6.0				\directx\directx\dxsetup 
        Vortex Application Setup			\Setup 
        PCI Multifunction Audio Device			\Win95


B  DIRECTX 6.0 INSTALLATION

    
    You may be prompted to install Microsoft DirectX 6.0 after Vortex driver 
    installation. 

	1.  When the DirectX setup panel opens, select "Reinstall DirectX". 
	    (Even if you do not have DirectX installed on your machine, the
	    Microsoft DirectX 6.0 setup program still asks if you wish to 
	    reinstall).

	2.  You may receive some prompts as to whether to replace specific 
	    DirectX files on your computer. If you have previously installed
          an older version of DirectX on your machine, be sure to replace 
          any sound-related DirectX drivers. Video DirectX drivers do not 
          need to be changed.

	NOTE:  You will be asked to reboot your machine when DirectX 6.0 
	installation completes. Reboot the PC when asked. Additional Vortex 
	drivers may continue to load when Windows restarts. 


C.  UNINSTALLING WINDOWS 95/98 DRIVERS

To uninstall the Vortex software, you can use the following procedure: 
	
	1.  Open to the Windows 95/98 Device Manager (right-click on "My Computer"
	    and select "Properties").
	2.  Open the "Multifunction Adapters" tree and select "Vortex 
	    Multifunction PCI Platform"
	3.  Press the "Remove" button at the bottom of the Device Manager 
	    window pane. 
	4.  The drivers are now removed from memory, but are still on the hard
	    disk. To delete the files from 
	    the hard disk:
		
		a.  Open the Windows 95/98 control panel's "Add/Remove Programs"
		    applet.
		b.  To remove the drivers, double-click "Aureal Vortex". A 
		    Vortex uninstaller application starts.
		c.  To remove the demo applications, double-click "Aureal 
		    Vortex Applications".  There is no need to reboot the 
		    computer.


For Technical Support please contact your board manufacturer.

Aureal. A3D, A3D-I, A3D-Interactive, and the Aureal logo are trademarks and 
Vortex is a registered trademark of Aureal Semiconductor Inc. 
All other trademarks are owned their respective owners.

================================================================================
Aureal Semiconductor, Inc.                      (c) 1996-98, All Rights Reserved
================================================================================
 