                Avance Logic AC'97 Sound System Software        ver: A3.30
                        Installation and Setup


Driver & Application Installation/Removal Procedure For Avance AC'97 Codec:
=================================================================================

<<< For Win98SE/Win2000/WinME/WinXP (WDM driver) >>>

---------------------------------------
Setup Driver/Application at first time:
---------------------------------------

Step 1. Before installing the Avance AC'97 Drivers & Applications, Press the
        [Cancel] button if Windows detect the PCI Multimedia Audio device. 
          
Step 2. Insert the "Avance AC'97 Drivers & Applications" CD into the CD-ROM 
        drive and run the setup.exe program to finish the installation. 

Step 3. Click on [Next/OK/Go] to continue the procedure. If the Windows popup 
        "Digital Signature Not Found" message, press [Yes] to continue the 
        installation.
        
Step 4. Finally, select to restart the system and press [Finish] to complete
        the installation.  

        The system will reload the drivers and do some adjustments in the INF
        file if so required.

--------------------------
Update Driver/Application:
--------------------------

Step 1. Follow Step 2,3,4 described in [Setup at first time] above to complete
        the procedure.

--------------------------
Remove Driver/Application:
--------------------------

Step 1. Go to Start\Settings\Control Panel.

Step 2. Select [Add/Remove Programs] icon.

Step 3. Select "Avance AC'97 Drivers and Applications" and press [Change/Remove]
        button.

Step 4. Click on [Next/OK/Go] to finish the uninstallation.        

Step 5. At the end of the procedure, select to restart the system and press
        [Finish] to complete the uninstallation.


<<< For Win98 Gold (First Edition) >>>

---------------------------------------
Setup Driver/Application at first time:
---------------------------------------

    The same procedure in Win98SE/Win2000/WinME/WinXP.

--------------------------
Update Driver/Application:
--------------------------

    The same procedure in Win98SE/Win2000/WinME/WinXP.
    
--------------------------
Remove Driver/Application:
--------------------------

    The same procedure in Win98SE/Win2000/WinME/WinXP.

<<< For WinNT 4.0 (NT4 driver) >>>

---------------------------------------
Setup Driver/Application at first time:
---------------------------------------

    Ignore Step 1, and follow the same procedure in Win98SE/Win2000/WinME/WinXP.

--------------------------
Update Driver/Application:
--------------------------

    The same procedure in Win98SE/Win2000/WinME/WinXP.
    
--------------------------
Remove Driver/Application:
--------------------------

    The same procedure in Win98SE/Win2000/WinME/WinXP.

<< Other Informations >>

--------------------
Silent Installation:
--------------------

Run "Setup -s -f2<path\LogFile>"
i.e. setup -s -f2c:\mylog.log 


Note: AVRack only works fine under WinNT 4.0 after installing
      Service Pick 3 or later.
---------------------
Version Informations:
---------------------

WDM driver for Win98SE/WinMe/Win2000/WinXP : 5.10.0.4010
WDM driver for Win98Gold                   : 5.10.0.5011
VXD driver for Win95/Win98Gold             : 4.5.0.3018
VXD Software wavetable driver              : 3.1.0.0
NT4 driver for Windows NT4                 : 4.3.0.3030
NT4 software wavetable driver              : 4.3.0.2001

RtlRack for Win98/Me/2000/XP               : 1.2.0.0
AvRack for Win95/NT4                       : 2002.4.3.1

Avance Sound Effect Manager(CPL)           : 1.5.0.30
Avance Sound Effect Manager for NT4        : 2.3

Driver/Application Setup Program           : 4.76

--------
History:
--------
A3.30 -
1.  turn on/off EAPD by GPIO for specific model
2.  correct EAX initial setting.
3.  support I3DL2 interface
4.  fix wake on ring problem
5.  support DirectSound 3D positional audio by using HRTF algorithm
6.  Add "Loudness" control for ALC202/ALC202A.

A3.29 -
1.  Add "S/PDIF IN/OUT Pass-Through" mode for specific model
2.  fix S/PDIF-In Realtime monitor noise issue
3.  fully support EAX compatible sound effect
4.  fix S1 suspend/resume failure problem for some specific model using SiS audio controller
5.  only disable "3D depth" line for specific model
6.  duplicate analog input source according to output channel mode
7.  support DirectSound hardware acceleration features by default
8.  fix WinDVD problem when enabling video acceleration

A3.26 -
1.  Improve compatibility with Agere software modem
2.  Improve recording quality when IDE was in PIO mode.
3.  Remove 3D Depth mixer line for some models

A3.23 -
1.  Add "Loudness" mixer control for ALC650 front channel.
2.  Add "SPDIF in pass through to SPDIF output" option for specific model.
3.  Remove 3D depth mixer line.
4.  Improve compatibility with WinDVD 4.0 playing AC3 bit stream through DirectSound API.
5.  Improve recording quality for some specific models.

A3.22 -
1.  Support S/PDIF-In function for ALC650 ver.E
    
A3.21 -
1.  Fix Front Mic problem.
2.  Turn off "Analog input bypass to surround" when enter D1 mode.
3.  Change back the default volume of Master to the middle position.
4.  Add "EnableDCVoltageControl" customized option for ALC202/ALC202A.
5.  Support customized DirectSound 2D/3D Acceleration (bypass kmixer).
    Add "EnableDS3DLibrary" customized option to enble it.
    It is turned off by default.
6.  Add "PreventRegisterReset" customized option for VIA8233.
7.  Only ALC201 series and ALC650 series can use "Enable 3.3V support" customized option.
    For ALC202/A, it is work autometically.
8.  Reset DMA when change state to Pause for ICH4 to fix HCT DiectSound failure in WinMe.

A3.13 -
1. To avoid mapping lost on Win98SE by raising IRQ level and adding TagCount before get mappings.
2. Disable "Phone Line" for some specific models.
3. Improve S/W SRC (if needed) quality to meet PC99 requirement.
4. Mute SPDIF while master volume was muted.
5. Improve EAX 1.0 compatible issue.

A2.94 -
1. Modify mixer control for multichannel output - master/front/surround/center/subwoofer line.
   The master volume/mute control will adjust all of front/surround/center/subwoofer volume/mute now to avoid confusion.
   The independent front/surround/center/subwoofer line offer volume control to balance the multichannel output.
2. Support "Front Mic" instead of Mic2.
3. Support Center and LFE output swap function.
4. Turn off analog input pass to surround function when suspend.
5. To avoid mapping lost on Win98SE (it can also fixed by QFE).
6. Improve S/W SRC (if needed) quality to meet PC99 requirement.
7. Mute SPDIF while master volume was muted.

A2.84 -
1.  Support ALC650.

A2.82 -
1. Support ICH4
2. Implement workaround for Intel 440MX audio controller
3. Set analog CD Maximum volume to 12dB.
   
A2.81 -
A2.80 -
1. Remove "SPDIF SRC" Node if turn on "Enable 48K SPDIF" option.
2. Turn on "Saving LED power" feature for G version
3. Save/Restore AC97 extended registers when Suspend/Resume
4. Modify Servie() function for set SPDIF Invalid bit.
5. Modify data 0 insertion method for SPDIF.
6. Fix C3/C4 issue.

A2.73 -
1.  Support ALC202A.

A2.71 -
A2.70 -
1.set CD Maximum volume to +12dB.

A2.62 -
A2.61 -
A2.60 -
1.  Fix 48KHz if SPDIF SRC was enabled.
2.  Fix NT4 driver for IRQ sharing on VIA8233A
   
A2.58 -
1.  Support ALC101.

A2.56 -
A2.55 -
1.  update VXD driver for VIA8233A.

A2.53 -
A2.52 -
1.  Support VIA8233A audio controller.
2.  Eliminate the PCM noise while playing AC-3 stream through SPDIF-out.
3.  Power down EAPD when master volume mute.
4.  Fix HCT full duplex unstable problem for VIA8233 audio controller.
5.  The driver now support only VID/DID/SVID/SSID entry for WHQL requirement

A2.51 -
A2.50 -
1.  Fix HCT ACPI stress device I/O test for VIA8233.
2.  Improve compatibility with software modem for power management.

A2.48 -
1.  The driver now support the VID/DID entry

A2.46 -
1.  Add customized options.
2.  Mute volume when volume slider was adjusted to the bottom.
   
A2.45 -
1.  Support ALC201A.
2.  The driver only support the VID/DID/SVID/SID entry to meet the
    INF requirement for PCI devices for WHQL logo.

A2.43 -
1.  Add SPDIF Mute control and SPDIF SRC On/Off control.
2.  Modify 3D depth control behavior.
    When the slider was adjusted to the bottom,
    the 3D depth will be turned off.
3.  Sound Effect Control Panel now installed by setup program.
    It will not be installed with INF file.
4.  AvRack support CD track auto-load function.

A2.42 -
1.  Add Mic2 select control
2.  Improve MR card compatibility
3.  Change volume default settings

A2.40 -
1.  Enable ALC201 3.3V function (INF optional)
2.  Auto Power down DAC/ADC (INF optional)
3.  Avoid scandisk problem on some machines
4.  Fix HCT system test for VIA 686 (ACPI / Stress Device I/O)
5.  Change version number to 5.10.00.xxxx for WinXP versioning requirement
6.  Save/Restore recording mux setting
7.  Improve compatibility with PCTel MR card
8.  Fix hang problem while burn-in PowerDVD on some machines.
9.  Fix IBM ViaVoice Mixer problem.
10. Add MIC 20dB Boost control on recording MIC source line
11. Add Subsystem IDs
