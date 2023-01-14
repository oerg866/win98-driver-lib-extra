                Avance Logic ALS4000 Sound System Software    ver:ALS40.A1.60
                        Installation and Setup


Windows95/98(VXD) Driver & Application Installation/Removal Procedure For ALS4000:
=================================================================================

First Time Driver/Application Installation:

Step 1. After installing the ALS4000 sound card into the PCI slot of your
        computer, turn on the system power. Windows 95 will prompt you with 
        a "New Hardware Found" dialog box. To install the Windows 95 driver,
        please select "Driver from disk provided by hardware manufacturer" 
        option and click on [OK].  

Step 2. Insert the "ALS4000 Windows95 Driver and Utilities" CD-ROM/disk into the
        appropriate drive and select that drive from the prompted dialog box and 
        click on [OK]. Windows 95 will copy all the needed files and set up all 
        the logic devices on the board automatically.

Step 3. Install the application(ALSRACK Player) by running the SETUP.EXE file 
        (included in the " Windows95 Drivers and Utilities" CD-ROM/disk) from
        the Windows 95 START MENU|RUN.  In selecting a setup type, please choose 
        "Install Application Only..." and click on [Next].  By doing so, setup 
        will install the bundled application into you computer system.  

Note:  See below for full description of ALSRACK functions.



Driver/Application Removal & Installation:

Step 1. To remove an existing driver/application and install with the latest 
        driver/application, please run SETUP.EXE file(inlcuded in the " Windows95 
        Drivers and Utilities" CD-ROM/disk) from the Windows 95 START MENU|RUN. 

Step 2. In selecting a setup type, please choose "Remove and Install Software.." 
        and click on [Next].  When asked with "Do you want to install the bundled 
        application?"  Select "Yes, I do." to install ALSRACK Player or "No, I 
        don't." if not.  Click on [Next] and the program will install both the driver 
        and application automatically.

Note:   If you have not installed the bundled application(ALSRACK Player) in step 
        #2 and wish to install later, you can run SETUP.EXE again and select "Install 
        Application Only.."
        The DOS driver will installed autometically if you install driver by
        running SETUP.EXE, and it will work when you shutdown your computer
        by choosing restart to MS-DOS mode.


Driver/Application Removal ONLY:

Step 1. If you want to remove an existing driver/application ONLY, you may do so by 
        running SETUP.EXE file (inlcuded in the " Windows95 Drivers and Utilities" 
        CD-ROM/disk) from the Windows 95 START MENU|RUN.

Step 2. In selecting a setup type, please choose "Remove Software.." and click on 
        [Next].  The program will remove all existing and associated driver files 
        automatically.





Troubleshooting:
================================================================================
If no sound or device does not function properly, please check 
CONTROL PANEL|SYSTEM|DEVICE MANAGER.  The list of audio related devices appear 
under the category of "SOUND, VIDEO & Game Controller.." should include the followings:

ALS4000 External Midi(MPU401) Device
ALS4000 Internal Midi(OPL3) Device
ALS4000 Joystick Device
ALS4000 PCI Audio Device
ALS4000 Wave Audio Device

Note:   If any of the above devices has an yellow exclamation mark next to it or appear 
        to be missing, please run SETUP.EXE again and choose "Removal and Install Software.." 
        to insure the above devices are properly installed.

If you want to play DOS game under real-mode DOS, please shutdown you computer
by choosing restart to MS-DOS mode. Please make sure that the DOS driver was
installed properly by running SETUP.EXE to install the driver.


ALSRACK for ALS4000
================================================================================
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
     to change the volume, or click balance LEFT or RIGHT arrow buttons to change 
     balance.
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
     to begin recording. When finished recording, push the record button (now it is 
     a red square) to stop.  After finished, save the file as the name you specified.     
3.4  Full-duplex:
     For sound card supporting full-duplex, TAPEI and TAPEII can work at the
     same time. This means while TAPEI is playing, TAPEII can record, or while
     TAPEII is recording, TAPEI can play. 
     When using full-duplex, the control buttons work like this:
     Playback button and stop button only take effect for TAPEI, record button
     works only for TAPEII. Push record button once to begin recording, and push it 
     again to stop recording.
3.5  Synchronous recording (record and play simultaneously):
     After selecting an INPUT media and new wave file for recording, push button 
     SYNC.REC to begin a synchronous recording. The mixer will automatically 
     play the source file and begin recording at the same time.


4.   CD
4.1  EDIT and Program:
     Push EDIT to select which tracks (selections on the CD) to play and add it to 
     the Playlist. Then click the Program button to play the selected tracks.
4.2  Random play:
     The Random button plays tracks in a random order.
4.3  Repeat:
     To repeat one track of a CD, select the track and push the repeat button one 
     time.
     A single repeat signal will appear in the CD player window.       
     To repeat the full CD, push the repeat button 2 times.
     A full repeat signal will appear in the CD player window.


Software Wavetable.
================================================================================
Current version of software wavetable driver will only mix with the following 
wave sample rates:  11K, 22K & 44K.  Any other samples selected will show device
in used message.  While using the wavetable driver, software wavetable(ALS4000 being default)
must be selected as the wave mapper device.  

Note:   Speaker icon at lower right corner will disappear as a result of this selection, 
        but this will be corrected in our next release of driver.

