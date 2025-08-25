Thursday 20/2/2003

3DLABS Windows 98/ME GRAPHICS DRIVER
====================================
Display Driver Build 4.12.01.3000-1536R

(c) Copyright 3Dlabs Inc. Ltd. 2003. All rights reserved worldwide.


** TO VIEW THIS FILE CORRECTLY IN NOTEPAD, ENABLE "WORD WRAP" FROM THE FORMAT MENU **


The material in this document is the intellectual property of 3Dlabs Inc. Ltd. While every care has been taken in the preparation of this document, 3Dlabs accepts no liability for any consequences of its use.  Our products are under continual improvement and we reserve the right to change their specification without notice.

3Dlabs, and Wildcat are registered trademarks of 3Dlabs Ltd., 3Dlabs Inc. Ltd., or 3Dlabs Inc. in the United States and/or other countries. Microsoft Windows, Windows NT, Windows 2000 and Direct3D are either registered trademarks or trademarks of Microsoft Corp. in the United States and/or other countries. Intel and Pentium are registered trademarks of Intel Corporation. AMD, K6 and Athlon are registered trademarks of Advanced Micro Devices (AMD), Inc. OpenGL is a registered trademark of Silicon Graphics, Inc. All other trademarks are acknowledged and recognized.



Contents
========

1.......Introduction
2.......Prerequisites
3.......Downloading And Installing The Drivers
3.1.............Downloading The Drivers
3.2.............Installing The Card
3.3.............Installing The Drivers
4.......Uninstalling
5.......Resolutions and Refresh Rates
6.......The 3Dlabs Control Panel
6.1.............The Information Tab
6.2.............The Setup Tab
6.3.............The OpenGL Tab
6.4.............The Direct3D Tab
6.5.............The Advanced Tab
6.6.............Supported Languages
7.......The Taskbar Utility
8.......Acuity Window Manager ("WinMan")
9.......General DirectX advice
10......Driver Release History
11......Known Anomalies
12......Trouble Shooting
12.1............Monitor Fails to Synchronize Following Boot
12.2............Windows 2000 Only Boots Into VGA mode
13......Customer Support



1. Introduction
===============
IMPORTANT
The 3Dlabs Wildcat VP drivers DO NOT SUPPORT the Wildcat4000, 4110, 4210, Wildcat II range(5000, 5110), or Wildcat III range(6110, 6210) of adapters. Please refer to 3Dlabs website www.3dlabs.com for drivers for the above products.

This Readme describes the Wildcat VP drivers for the 3Dlabs Wildcat VP range of graphics adapters. Supported adapters are:

• Wildcat VP560
• Wildcat VP760
• Wildcat VP870
• Wildcat VP970

Once the driver has been installed the display driver release number can be determined by starting the Display Applet in the Control Panel folder. Press the "Advanced..." button, then Select the "3Dlabs" tab. The Driver version number can be found at the bottom of the Hardware Information section. The x.yy-zzzz code uniquely identifies the driver build.



2. Prerequisites
================
• Windows 98 or Windows ME
• Supported CPUs: Intel Pentium II, III, 4 processors or later, AMD K6 and Athlon processors or later.



3. Downloading And Installing The Drivers
=========================================

3.1. Downloading The Drivers
============================

To download the drivers from the 3Dlabs website, go to the Drivers section of http://www.3dlabs.com and select the appropriate drivers for your card, then download the file into an appropriate scratch directory (e.g. C:\3dlabs).

3.2. Installing The Card
========================

To install your 3Dlabs graphics adapter:-

1. Shutdown the computer and power-off.
2. Insert the adapter, power-on and boot-up into Windows 98 or Windows ME.

After logging-in the Hardware Wizard will appear. These drivers are provided with their own installer so you should hit the cancel button for any "Found New Hardware" dialogs that appear.

3.3. Installing The Drivers
===========================

Go to the directory where you downloaded the drivers and run the self installing .exe file that you downloaded. This launches the '3Dlabs Graphics Driver Setup' program, which will guide you through the process of installing your driver. The setup program will ask you for confirmation before installing any drivers. You should hit the "Yes" button each time.

Once setup has completed, you will need to reboot your system in order for the drivers to load.



4. Uninstalling
===============
The Control panel extension and the application support tool can be uninstalled by following this procedure:

1. Open the Add/Remove Programs icon in the Control Panel.
2. Highlight the "3Dlabs Desktop Tools" in the list and click "Add/Remove".
3. Follow the instructions to complete the removal of the control panel and application support tool.



5. Resolutions and Refresh Rates
================================
The resolutions supported (and maximum refresh rate) for the Windows Desktop are dependent on your graphics card.

The color depths supported are:
	256 colors (Paletized)
	High Color (16 bits per pixel)
	True Color (32 bits per pixel)

Many refresh rates are supported for all of these modes. The refresh rate available is typically limited by your monitor type. The monitor type will be auto detected by Windows if your monitor supports DDC. If windows does not recognise the monitor, you will be prompted to install the monitor information disk from your monitor manufacturer. If your monitor does not support DDC, then you will have to select a monitor type manually from the display control panel.

A combination of the DDC information and the monitor type is used by Windows to determine which modes are available at which refresh rates.

NOTE: If you have an unknown monitor type, the driver will set the refresh rate for all modes to 60Hz - which may flicker noticably on your monitor.



6. The 3Dlabs Control Panel
===========================

To access the 3Dlabs Control Panel, launch the Display Properties Control Panel, select the "Settings" tab, click the "Advanced..." button and select the "3Dlabs" tab. This tab shows basic information for your adapter and its drivers including the chipset type, board name, amount of physical memory on the board, the RAMDAC type, BIOS version, and Driver version.

The driver version number is in the form a.bb.cc.dddd-zzzz and uniquely identifies the driver build.

Hitting the "Advanced..." button on this page loads the 3Dlabs control panel. The 3Dlabs control panel is split into a number of pages as listed below. The pages are selected by clicking on one of the configuration tabs at the top right of the window.

The 3Dlabs tabs support Tool Tips help. To find out more about a particular option, hover your mouse over the relevant item and a help bubble will appear.

6.1. The Information Tab
========================

This page gives more detailed information on the OpenGL and DirectX drivers.

6.2 The Color Control Tab
=========================

This tab allows you to adjust the brightness, contrast and gamma correction of your display to compensate for different monitors and ambient lighting conditions.

6.3 The OpenGL Tab
==================

This tab allows you to tune the following parameters of your OpenGL driver setup:
• Full Scene Antialiasing
• Buffer Swap Mode
• Z Buffer Depth
• Texture Color Depth
• Texture Filtering
• Wait for Vertical Synch
Hover the mouse over each item to learn more about the settings using the Tool Tips Help.

Optimized Applications
~~~~~~~~~~~~~~~~~~~~~~
Allows you to choose which OpenGL application the driver is presently optimized to run. Use the pull down menu to optimize the driver configuration for a different application, or select "OpenGL(tm)Default" for a good all round setting.

You can create your own optimized setting. To do this:
1.) Choose a setting for an application which is similar to the one you want.
2.) Click the "Create Copy" button to create a copy and rename it in the pull down menu window.
3.) Change the settings as appropriate.
4.) Click the "Save" button.
You can also delete your own customized settings (but not those that come preset in the driver).

Dual Monitor OpenGL Options
~~~~~~~~~~~~~~~~~~~~~~~~~~~
This control is only required under Windows 2000 and Windows XP, so has no effect under Windows 98/ME.

Wait for Vertical Synch
~~~~~~~~~~~~~~~~~~~~~~~
Smooth animation of 3D applications can be achieved by rendering to an off-screen color buffer and copying or swapping the contents to the displayable front buffer at the completion of each frame. Enabling this option prevents tearing of the display (often visible as flickering horizontal lines), by synchronizing the swap of the back and front buffers to the vertical blank retrace interval of the monitor display.

6.4 The Direct3D Tab
====================

This tab allows you to tune the following parameters of your Direct3D driver setup:
• Full Scene Antialiasing
• Force Z Buffer Depth
• Wait for Vertical Synch
Hover the mouse over each item to learn more about the settings using the Tool Tips Help.

Optimized Applications
~~~~~~~~~~~~~~~~~~~~~~
Allows you to choose which Direct3D application the driver is presently optimized to run. Use the pull down menu to optimize the driver configuration for a different application, or select "Direct3D Default" for a good all round setting.

You can create your own optimized setting. To do this:
1.) Choose a setting for an application which is similar to the one you want.
2.) Click the "Create Copy" button to create a copy and rename it in the pull down menu window.
3.) Change the settings as appropriate.
4.) Click the "Save" button.
You can also delete your own customized settings (but not those that come preset in the driver).

Wait for Vertical Synch
~~~~~~~~~~~~~~~~~~~~~~~
Smooth animation of 3D applications can be achieved by rendering to an off-screen color buffer and copying or swapping the contents to the displayable front buffer at the completion of each frame. Enabling this option prevents tearing of the display (often visible as flickering horizontal lines), by synchronizing the swap of the back and front buffers to the vertical blank retrace interval of the monitor display.

6.5 The Advanced Tab
====================

Enable Taskbar Shortcut
~~~~~~~~~~~~~~~~~~~~~~~
Allows you to enable and disable the taskbar application which provides quick access to main features of the control panel. When the taskbar application is enabled it will be placed on the taskbar (system tray) each time the system is booted. Disabling the taskbar application from the setup page means that the application will not appear each time you reboot. 

Pipeline Optimizations
~~~~~~~~~~~~~~~~~~~~~~
Enables you to optimize your graphics adapter for maximum geoemetry throughput (ideal for CAD/CAM applications), or texture fill rate (ideal for games and texture intensive modelling applications). This setting affects applications using either the OpenGL or DirectX APIs.


6.6 Supported Languages
=======================

The 3Dlabs control panel supports the following languages: -

Chinese (Simplified)
Chinese (Traditional)
Dutch
English
French
German
Italian
Japanese
Korean
Spanish



7. The Taskbar Utility
======================

The task bar utility provides quick access to some of the facilities on the control panel. To access the application right click on the 3Dlabs icon in the taskbar. Full documentation is provided through the "Help" item on the pop-up menu.



8. Acuity Window Manager ("WinMan")
===================================
The Acuity Window Manager, WinMan for short, is a tool that provides extra windowing and desktop features that are of particular use in multi-monitor configurations. 

For example, WinMan can control the positioning of dialog boxes : a useful feature because their default positions are generally inconsistent, which can become annoying on multi-monitor systems. 
Another example : WinMan will also let you partition your desktop into any number of 'virtual' desktops; useful for users who keep a large number of applications open at once.

WinMan may be configured and enabled from either the wizard that appears after driver installation, or from the popup menu of the Taskbar Utility described above.



9. General DirectX advice
=========================

This driver requires DirectX8 to be installed, otherwise DirectX applications will not run.

Some games ( e.g. Unreal ) give you the option to install DirectX binaries during the game installation. The game
may attempt to force-install older versions of DX binaries over your current DX binaries. This will almost certainly lead to the game failing to start up.

You can determine your DirectX version by running the display control panel and clicking on the 3Dlabs tab and
then the Advanced tab. The DX version is in the DirectX Information pane in the form:

		DirectX Release:	4.XX.YY.ZZZZ

where XX is the number you require. For example you may see

		DirectX Release:	4.08.01.0881

and so you have DirectX 8 installed. Now, when a game installer runs you can decline the offer to install the old DX binaries.



10. Driver Release History
==========================

Current Release
===============
• This is the first release of the 3Dlabs Wildcat VP Drivers



11. Known Anomalies
===================

Here is the current list of known problems with the driver:

3ds max
~~~~~~~
We recommend that for best results you select the OpenGL renderer for the 3ds max 4.x versions, and the Direct3D renderer for 3ds max 5.x and later.

3Dlabs Help page
~~~~~~~~~~~~~~~~
The Find tab on the 3Dlabs help page does not work.

Morrowind
~~~~~~~~~
You may see artifacts in some special effects in Morrowind. To work around this problem please disable the pixel shaders in the in-game options menu.

Aliens vs. Predator2
~~~~~~~~~~~~~~~~~~~~
There is a problem with the grenade launcher target when out of ammunition. To workaround this problem please run the game at 16bpp.

Half-Life
~~~~~~~~~
You will need to download the patch for at least version 1.0.0.8 from www.sierra.com to use hardware accelerated OpenGL. Without this patch some elements are rendered without textures.

VIA based motherboards
~~~~~~~~~~~~~~~~~~~~~~
You should upgrade to the latest drivers from http://www.viatech.com/drivers/. The AGP drivers should be installed in Normal mode - do not install in Turbo mode.



12. Trouble Shooting
====================

12.1. Monitor Fails to Synchronize Following Boot
=================================================

Your display mode is probably too high a resolution. Reboot the system and at the DOS "OS loader screen" hit <F8> and select the "Safe Mode" boot option. Using the display properties applet set the display to 640x480x8bpp and the monitor to 60Hz refresh. Reboot again and set the monitor to the desired mode (obviously, lower than the mode causing the problems!)

12.2. Windows Only Boots Into VGA mode
======================================

You may have incorrectly installed the drivers. Try reinstalling the drivers, if the problem persists, look on the 3dlabs website for a driver upgrade.



13. Customer Support
====================
You can contact 3Dlab's technical support via the World Wide Web at www.3dlabs.com, or via email to support@3dlabs.com.
