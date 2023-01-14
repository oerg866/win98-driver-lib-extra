                Avance Logic ALS300 Sound System Software
                        Installation and Setup



DOS and Windows 3.1 Installation for ALS300:
====================================================

[SETUP.EXE for Windows 3.1]

The SETUP.EXE is a Windows 3.1 setup program that installs DOS and Windows
3.1 drivers and utilities.

The user can run SETUP.EXE by selecting File|Run... and typing "A:SETUP" on
the command line under Windows 3.1 Program Manager, or by typing "A:SETUP" at
DOS prompt if Windows directory is in the PATH. The SETUP.EXE copies all the
DOS drivers and utilities to the directory that user specifies during the
setup program.  All the Windows 3.1 drivers and VxDs are copied to the 
Windows system directory.  When the user installs the Avance Sound System
for the first time the APCONFIG.EXE is started to configure the board setting
after the Setup program is finished.

[DOSINST.EXE for DOS Only installation]

The DOSINST.EXE is a DOS installation program that copies all the DOS drivers
and utilities to the directory that user specifies.  When the user installs
the Avance Sound System for the first time the APCONFIG.EXE is started to
configure the board setting after the Setup program is finished.  DOSINST.EXE
can be installed by typing A:DOSINST.EXE at the DOS prompt.


Windows 95 installation procedure for ALS300:
=====================================================

1. After user installs the ALS300 sound card into the PCI slot in the
   computer and powers on the system, Windows 95 will prompt user with a "New
   Hardware Found" dialog box To install the Windows 95 drivers, select
   "Driver from disk provided by hardware manufacturer" and click on OK.

2. Insert the "ALS300 DOS/Win3.1/Win 95 Drivers and Utilities" CD-ROM
   into the appropriate drive and select that drive from the prompted dialog
   box and click on OK. Windows 95 will copy all the needed files and set up
   all the logic devices on the board automatically.

3. Install the ALSRACK player by running the SETUP.EXE file (also provided
   on the "ALS300 DOS/Win3.1/Win 95 Drivers and Utilities" CD-ROM) from
   the Windows 95 Start menu|Run.  This will create the Avance Sound Program
   Group with the ALSRACK utility icon.  
   (See Appendix below for full descr of ALSRACK functions).

4. For the first time insatllation, please reboot the system to enable
   legacy DOS game support.


Troubleshooting:
================

This appendix provides some tips and information for some of the 
problems you might encounter with your ALS300 sound card either during
installation or normal use.

[Problems in DOS]

Problem:        No sound in a DOS application
Cause:          There could be conflicts in the SB16 settings.
Solution:       Rerun the C:\ALSPCI\APCONFIG.EXE and try another Port,
                DMA, or IRQ.

[Problems in Windows 3.1]

Problem:        There is no "Sound..." or "MIDI Sequencer..." item 
                under the menu "Device" in the Media Player. 
Cause:          Mixer driver is not loaded.
Solution:       Open the SYSTEM.INI file with any file editor. You 
                should see the following: 
                [drivers]
                Wave=alpci31.drv
                Aux=alpci31.drv
                Mixer=alpci31.drv
                Midi=alpci31.drv

                [386Enh]
                device=alpcisnd.386

                [boot]
                drivers=mmsystem.dll msmixmgr.dll


Problem:        Third party mixer application with Sound Blaster compatibility
                will not run with Avance Sound System.
Cause:          Avance Sound System is Microsoft Sound System compatible. Avance
                Logic, Inc. does not support previous Sound Blaster Mixer Interface.
Solution:       Use ALSRACK.EXE application that is shipped with this disk.


Problem:        CD audio will not play after the ALS drivers are installed.
Cause:          The user did not install the [MCI]CD-AUDIO driver.
Solution:       Manually add [MCI]CD-AUDIO driver via Control Panel.

        
Appendix - Driver Reference:
============================

[Windows drivers]
ALS300 has three sets of driver and one set VxD for Windows 95 and
Windows3.1. They are listed below:

                Sound System Driver     OPL3 Driver     MPU401 Driver
Win95 Drivers   Alpcisnd.drv            Alpcisnd.drv    Alpcisnd.drv
Win95 VxDs      Alpcisnd.vxd            Alpcisnd.vxd    Alpcisnd.vxd
Win3.1 Drivers  Alpci31.drv             Alpci31.drv     Alpci31.drv
Win3.1 VxDs     Alpcisnd.386            Alpcisnd.386    Alpcisnd.386


The Windows 95 joystick drivers are the MSJSTICK.DRV and VJOYD.VXD 
that are Microsoft drivers shipped with Windows 95. Besides these 
Windows 95 drivers and VxDs, a PCISOUND.INF is needed for Windows 95
installation.

For Windows 3.1, drivers and VxDs have to be specified in the SYSTEM.INI 
file and be loaded when the Windows 3.1 starts. The entries listed in below 
should be added to SYSTEM.INI file by the setup program.

        [386Enh]                        [drivers]
        device = alpcisnd.386           wave  = alpci31.drv
                                        mixer = alpci31.drv
                                        aux   = alpci31.drv
                                        midi  = alpci31.drv

!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!                                                                             !
! IMPORTANT NOTES:                                                            !
!       Either you setup under windows 95 or windows 3.1, you MUST insure     !
! that the drivers or VxDs files of old sound card have been removed from your!
! windows's system directory. Otherwise, even if you setup properly, the new  !
! sound card maybe still not work.                                            !
!                                                                             !
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!


[DOS drivers]
The DOS drivers include LEGACY.COM, APSINIT.EXE, and APCONFIG.EXE.

LEGACY.COM
----------
The LEGACY.COM is a DOS TSR program for compatibility with the legacy device.
It have to be loaded for the game which use the legacy sound device under
DOS and DOS BOX in Windows.
After the installation, the setup program will modify the autoexec.bat and
make it to load the LEGACY.COM when you boot-up your computer.
You need to reboot the system to enable it at the first time installation.
This program will be called by APSINIT.EXE autometically.

APSINIT.EXE
-----------
The APSINIT.EXE initializes the Avance sound chip ALS300. It is
specified in the AUTOEXEC.BAT file followed by a path name as below.
                C:\alspci\apsinit.exe C:\Win31
APSINIT.EXE and APCONFIG.EXE use the path that follows the APSINIT.EXE
in the AUTOEXEC.BAT to find the initial data file ALSPCI.INI. The ALSPCI.INI
file will be copied to the Windows directory or the same directory as
APSINIT.EXE for DOS-only installation. The Windows sound system driver
ALPCI31.DRV and the Windows sound rack application ALSRACK.EXE also share
ALSPCI.INI file for initial values.

APCONFIG.EXE
------------
The APCONFIG.EXE is a DOS program to help users change the IO, IRQ,
and DMA resource for the Avance sound system on board devices and to 
test the new settings through playing the STEST8.WAV, STEST16.WAV, 
and FMTEST.MID test files. The new settings are saved in the ALSPCI.INI
file which will be used when APSINIT.EXE initializes the board.

Information Files:
------------------
PCISOUND.INF is a installation information file for Avance Logic ALS300
sound chip under Windows 95. This file tell Windows 95 where the drivers should
be copied during installation.
See the instructions above for ALS300 Windows 95 installation.

ALSRACK for ALS300
------------------
1.   Structure and components:
     The ALSRACK consists of a MIXER control panel, MIDI panel, WAVE panel, 
     and CD panel.
1.1  To enable or disable a panel:
     Clicking the mouse button on the MIDI, WAVE, or CD in MIXER control panel 
     will cause the corresponding panel to disappear, another click will cause the
     corresponding panel to re-appear.
1.2  To change a channel:
     Click channel LEFT or RIGHT button to change to the channel you want.
1.3  To activate volume and balance control:
     Change to the channel you want (see 1.2), then click up or down arrow buttons 
     to change the volume, or click balance LEFT or RIGHT arrow buttons to change balance.
1.4  To mute system:
     Change to the channel you want, then click MUTE check mark to disable sound,
     click again to re-enable sound.


2.   MIDI panel
2.1  To open or close a MIDI file:
     Click the button of the MIDI sign on the MIDI panel, choose OPEN to open a
     MIDI file, or choose CLOSE to close a file.
2.2  Auto repeat and show information:
     Click the button of the MIDI sign on MIDI panel.  Clicking on AUTO REPEAT or
     SHOW INFORMATION will enable or disable the selection. When AUTO REPEAT is
     selected, the MIDI file will be played again when it reaches the end.
     When SHOW INFORMATION is selected, the MIDI window will open and the
     information from the MIDI file will appear on the MIDI window. When a MIDI
     file is opened, you can also click the MIDI window to show the information of 
     that file.
2.3  Other operations:
     When a MIDI file is opened, you can click PLAY to play it, or click PAUSE,
     STOP, FF or RW to manipulate the selection. You can also use the volume control
     buttons on the MIDI panel to control the volume directly.


3.   WAVE panel
3.1  Select TAPE I or TAPE II to playback:
     There are two TAPE boxes on the WAVE panel. TAPE I can only play wave
     files. TAPE II can play and record wave files. There is one set of
     control buttons on the right of WAVE panel. When Tape I is selected,
     the control buttons will take effect for TAPE I. When Tape II is selected,
     the control buttons will work for TAPE II. Click the button
     TAPEI/TAPEII to select between TAPEI or TAPEII, or push the button TAPEI
     PLAYBACK on TAPE I box to select TAPE I, while pushing the button TAPEII REC/PLAY
     on TAPE II box to select TAPEII. 

Note: When you want to playback a wave file, you need to select TAPE I/TAPE II first.

3.2  Open a wave file to play:
     Push the OPEN button, select OPEN on the menu, select a wave
     file to play. When the wave file is opened, the TAPE containing the
     file is automatically selected, just push the PLAY button to play it.
3.3  Record a wave file:
     Push the button REC.INPUT to select the input media (Line in, MIDI, 
     Audio CD, or MIC), then push the the button OPEN on TAPE II and select NEW 
     to create a new wave file.  The TAPEII indicator will be red to show it
     is waiting to record.  Play the source media, and push recording button on TAPEII 
     to begin recording. When finished recording, push the record button (now it is a
     red square) to stop.  After finished, save the file as the name you specified.     
3.4  Full-duplex:
     For sound card supporting full-duplex, TAPEI and TAPEII can work at the
     same time. This means while TAPEI is playing, TAPEII can record, or while
     TAPEII is recording, TAPEI can play. 
     When using full-duplex, the control buttons work like this:
     Playback button and stop button only take effect for TAPEI, record button
     works only for TAPEII. Push record button once to begin
     recording, and push it again to stop recording.
3.5  Synchronous recording (record and play simultaneously):
     After selecting an INPUT media and new wave file for recording, push button 
     SYNC.REC to begin a synchronous recording. The mixer will automatically 
     play the source file and begin recording at the same time.


4.   CD
4.1  EDIT and Program:
     Push EDIT to select which tracks (selections on the CD) to play
     and add it to the Playlist. Then click the Program button to play the selected tracks.
4.2  Random play:
     The Random button plays tracks in a random order.
4.3  Repeat:
     To repeat one track of a CD, select the track and push the repeat button one time.
     A single repeat signal will appear in the CD player window.       
     To repeat the full CD, push the repeat button 2 times.
     A full repeat signal will appear in the CD player window.


[ Known bugs - Beta version ]

1. The APCONFIG.EXE may not work well during setup process in Windows 3.1.

2. This beta version only support for PnP emulation was enabled.
   You can see the property page of PCI Sound Chip to check if your system
   is PnP emulation enabled or not.
   To see the property page, you need to open control panel first.
   Run the SYSTEM and choose Device Manager/Sound,video and game controlers\
   ALS300 PCI Sound Chip/Settings.
