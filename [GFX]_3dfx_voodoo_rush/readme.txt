Voodoo Rush(TM) based Single Planar Board Drivers

Voodoo Rush Driver kit Version: 3.01.00
Voodoo Rush Glide(TM) Driver Version: 2.48.00.0455
Voodoo Rush Glide3 Driver Version: 3.04.00.0455
Voodoo Rush DirectX(r) Driver Version: 2.17
2D Alsc. Display Driver Version: 4.10.01.2073
OpenGL(r) Driver Version: 1.0.0.0438 ICD

Copyright ( 1996/1997/1998/1999 3dfx Interactive, Inc. )
Copyright ( 1997 Alliance Semiconductor )
All Rights Reserved

NOTE: Use of this software is subject to the terms in the 3dfx license 
agreement.

3dfx Interactive, Inc.
http://www.3dfx.com

This product may be covered by one or more of the following
US patents: 5,724,561  5,740,343


=======================================================================
What's in the distribution?
=======================================================================
This distribution contains DirectDraw(r) and Glide drivers for Voodoo Rush
when running with Alliance AT25 (AT3D). The DirectDraw portion of the 
drivers supports Direct3D when using DirectX 5.0.

=======================================================================
Installation 
=======================================================================

Requirements
Requirements
------------

- Windows(r) 95/98
- PC with an Intel(r), AMD(r) or, Cyrix(r) based processor
- 16MB of RAM
- DirectX 5.0 or higher

Upgrade Existing AT25/Voodoo Rush Drivers
-----------------------------------------

1) Start Windows 9x
2) Extract the files for the AT25/Voodoo Rush driver to a directory.
3) Click Start, Contol Panel.  Double-click on Display.
4) Click the settings tab
5) Click Change Display Type
6) Under Adapter Type, Click Change
7) Click Have Disk
8) You will be prompted as follows:

     Windows 95 Standard Release users: Enter the path to the extracted drivers

              Windows 95 OEM SR2 users: Click the Next Button, no updated
					drivers will be found.   Click on
					"Other Location" then enter the path
					to the extracted drivers.
		Windows 98 users: Click "Update Driver" then click
                                        the Next Button twice on the
                                        Detection Dialog Box. Ensure that
                                        "Specify a Location" is checked and
                                        "Microsoft Windows Update" is not
                                        checked. Click Browse to continue.

9) When asked to choose a device, select "Alliance 3D + Voodoo Rush"
10) You may then be prompted to insert the Windows 95 Alliance 3D + Voodoo
    Rush Driver Disk.  Enter the path to the drivers again.
11) Windows will copy the drivers.   Reboot the system when prompted
12) Install DirectX 5.0 or higher


Fresh Installation 
------------------

NOTE: It is suggested that the extracted drivers be copied to a
floppy when executing a fresh installation.

1) Before removing your existing 2D card switch the video driver to 
   Standard VGA
2) If you have an exisiting 3dfx Voodoo based card also remove the 
   following key:
    HKEY_LOCAL_MACHINE\Hardware\CurrentControlSet\DirectDrawDrivers
3) Power off system and remove your existing 2D card and any Voodoo 
   based cards
4) Install the AT25 and Voodoo Rush Combo Card in a free PCI Slot
5) Power on the system and verify that video appears during post
6) Start Windows 95

  (Once Windows 95 starts you may be notified that no video device
   exists, click Cancel if this message appears)

7) Windows 95 will detect a new VGA Compatible Display, you need to:
     Windows 95 Standard Release users: Select "Use Driver from Mfr"
                                        and click OK
              Windows 95 OEM SR2 users: Click the Next Button on the
                                        Detection Dialog Box
  		Windows 98 users: Click the Next Button twice on the
                                        Detection Dialog Box. Ensure that
                                        "Specify a Location" is checked and
                                        "Microsoft Windows Update" is not
                                        checked. Click Browse to continue.

8) Point the driver location to where the files are extracted to and click
   OK.  (Windows 98: You will need to click on Next to continue)

9) You MAY then be prompted to insert the "Voodoo Rush Drivers for Windows 9X"
   Disk.  Enter the path the drivers are extracted to and press OK.

10) Windows will copy the drivers. Reboot the system when prompted

11) Install DirectX 5.0 or higher (If not already installed)


Limitations
-----------

Running 640x480,16 Color will run SUPERVGA.DRV or VGA.DRV.  No Voodoo 
Rush features will be used.  Switch to a different resolution or color depth.


OpenGL(r) ICD: Known Limitations
----------------------------------
The OpenGL ICD included with this kit is meant for use with OpenGL based 
games only. It may not be compatible with other applications that use the 
OpenGL API for 3D rendering support.

