Voodoo Banshee Windows(r) 98 AGP/PCI Driver Kit
--------------------------------------
Voodoo Banshee(tm) Driver kit: 1.04.00
Voodoo Banshee Win9x 2D/3D Display Drivers: 4.12.01.1222
Voodoo Banshee Glide(tm) 2.X Driver:  2.61.00.0518
Voodoo Banshee Glide 3.X Driver:3.10.00.0518
Voodoo Banshee Control Panel: 4.12.01.1552
OpenGL(r) Driver Version: 1.0.0.0508 ICD

Copyright ( 1998-2000 3dfx Interactive, Inc. )
All Rights Reserved

NOTE: Use of this software is subject to the terms in the 3dfx license 
agreement.

3dfx Interactive, Inc.
Website: http://www.3dfx.com

This product may be covered by one or more of the following
US patents: 5,724,561  5,740,343  5,808,621  5,822,452  5,831,624


=======================================================================
What's in the distribution?
=======================================================================
This distribution contains Voodoo Banshee drivers, control panel for 
Windows 98. The DirectDraw portion of the drivers supports Direct3D 
when using DirectX 7.0

NOTE: DirectX 7.0 redistributable files should be used with these 
drivers!

=======================================================================
Installation 
=======================================================================

Requirements
------------

- Windows 98
- PC with a Pentium, Pentium II, or Pentium Pro Processor and a free 
  AGP/PCI slot
- 16MB of RAM

Fresh Installation 
------------------

NOTE: Complete Steps 1 and 2 before removing your existing 2D card.

1) Extract the files for the Voodoo Banshee driver to a directory.
2) Before removing your existing 2D card switch the video driver to 
   Standard VGA. Click Start, Control Panel. Double-click on Display.

   Select 640X480 and 16 colors.  Accept the changes.

3) Power off the system and remove your existing 2D card.
4) Install the Voodoo Banshee Card in a free AGP/PCI Slot
5) Power on the system and verify that video appears during post.
6) Start Windows in Normal mode

  (Once Windows starts you may be notified that no video device
   exists, click Cancel if this message appears)

7) Windows will detect a new VGA Compatible Display. You need to:

                            Windows 98: Click the Next Button on the Detection 
                                        Dialog Box and in the "Specify a 
                                        Location" field click the checkbox 
                                        then enter the path to the Win98
                                        directory in the drivers location.

8) You may then be prompted to insert the Windows 98 AGP/PCI Voodoo Banshee Driver Disk.  
   Again, enter the path you specified in Step 1 and press OK.
9) Windows will copy the drivers. Reboot the system when prompted
10) Install DirectX 7.0.


Upgrade Existing Voodoo Banshee Drivers
--------------------------------

1) Start Windows 98
2) Extract the files for the Voodoo Banshee driver to a directory.
3) Click Start, Control Panel.  Double-click on Display.
4) Click the Settings tab then click:

                      Windows 98 users: Click "Advanced Properties"

5) Then under "Change Display Type/Advanced Display" click "Change"
6) Click "Have Disk" and enter the path specified in Step 2 plus:

                      Windows 98 users: the Win98 directory.

7) When asked to choose a device, select "3dfx Voodoo Banshee"
8) You may then be prompted to insert the Windows 95 Voodoo Banshee Driver Disk.
   Enter the path you specified in Step 2 again.
9) Windows will copy the drivers.   Reboot the system when prompted.
10) Install DirectX 7.0


Limitations
-----------

Running 640x480 16 Color will run SUPERVGA.DRV or VGA.DRV.  No Voodoo Banshee 
features will be used.  Switch to a different resolution or color depth.
Full windowed hardware acceleration with this version of the drivers is 
only possible when running at 16bpp modes.

Troubleshooting
---------------

####

Problem: After installing the card, the system still detects my old 
card even though it is no longer in the system.
Resolution: See Step 2 of the "Fresh Installation" instructions.

