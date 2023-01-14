
                          Additional Information

                 AZTECH WaveRider Platinum-3D version 1.00


   This file contains additional information and changes about the product
   that was not available at printing time.


   Playing DOS Games after Shutdown/Restart to Win95 DOS Mode
   ==========================================================
   
   The default configuration does not support playing DOS Games in Win95
   MS-DOS mode. It can only support playing games in Win95 MS-DOS Prompt Box
   (DOS Shell).

   An utility (DOSMODE.EXE) was included in the installed {\WAVRIDER\DOSMODE}
   directory which run a DOS Configuration Utility (AZTPNP.EXE) in the system's
   startup files (AUTOEXEC.BAT and DOSSTART.BAT) for configuring the card when
   restarting in MS-DOS mode to play DOS games.

   However, as default settings used in configuring the card under DOS mode
   may differ from the actual settings used by Win95, this may resulted in
   resource conflict in some cases. Please check the settings used by the
   sound card under Win95 against the default settings recorded in AZTPNP.CFG
   file in {\WAVRIDER\DOSMODE} directory prior to running the (DOSMODE.EXE)
   DOS utility.  

   NOTE : IF YOU HAD ALREADY RAN THE DOSMODE.EXE UTILITY AND DECIDED TO MADE
          MODIFICATIONS TO THE DOS DEFAULT SETTING. THE AZTPNP.CFG IS NOW 
          LOCATED IN THE ROOT DIRECTORY {C:\} AND NOT IN {WAVRIDER\DOSMODE}
          DIRECTORY.

   To determine the identical settings used in Win95 as well as in MS-DOS 
   mode, first go to "CONTROL PANEL" menu, double click on the "SYSTEM" 
   applet. You should then refer to the "RESOURCES" tab in Win95's "DEVICE 
   MANAGER".

   The Audio device entry under "Sound, Video and Games Controllers settings"
   section is usually named as "Audio Device (AZT1023)". 
   The following are the settings normally used :-

   --->Input/Output Range     0220 - 022F     ** Sound Blaster I/O Address **
       Input/Output Range     0388 - 038F     
       Input/Output Range     0534 - 0537
   --->Interrupt              05              ** Sound Blaster IRQ **
       Direct Memory Access   01      
   --->Direct Memory Access   03 or 00 (depend on system), 
                                              ** SB DMA used under DOS Box **

   Likewise, for the MPU-401 Device, Gameport and Joystick Device.
   

   Ensure that all the settings (SB I/O,IRQ and DMAs) displayed above matches
   the settings recorded in the default file (AZTPNP.CFG - listed below) in
   order for the proper operation of the card under MS-DOS mode.

   Below are the partial listing of the AZTPNP.CFG file.

       [DEVICE_01]                  ** Audio Device (AZT1023) **
       Description=AUDIO
       .
       .
   --->Port0=220         ** Sound Blaster I/O **
       Port1=388         ** FM Music I/O **
       Port2=534         ** Windows Sound System I/O **
   --->IRQ0=5            ** Sound Blaster IRQ  **
   --->DMA0=1            ** Sound Blaster DMA used under MS-DOS mode **
       DMA1=3            (This 2nd DMA is not used by DOS games)
    
 
       [DEVICE_02]                  ** MPU401 Device (AZT1023) **
       Description=MPU401 MIDI
       .
       .
   --->Port0=330         ** General MIDI I/O **
       IRQ0=9            (Not used in DOS games)

 
       [DEVICE_03]                  ** Gameport Device (AZT1023) **
       Description=GAME PORT
       .
       .
   --->Port0=200         ** Gameport/Joystick Port I/O **


       IT IS POSSIBLE THAT THE ABOVE DEFAULT SETTINGS MAY DIFFER FROM THE
       ORIGINAL SETTINGS USED BY WIN95. IT IS RECOMMMENDED THAT YOU SHOULD
       STICKS TO THE ORIGINAL SETTINGS USED IN THE WIN95 AND MADE CHANGES TO 
       THE VALUES IN THE AZTPNP.CFG LOCATED IN THE ROOT DIRECTORY ACCORDINGLY.

       

   DOS/Windows 31 Support
   ======================

   The WaveRider Platinum-3D card works best in Widnows 95 with its support
   for the Aztech Compund Synthesis Engine (96 Voices) enabled. This Software 
   WaveTable Synthesis works only in Windows 95 platform.

   To use this card in DOS or Windows 3.1x, you need to install the Aztech
   PnP Configuration Software from the bundled MIDI Music Workstation CD found
   in the {\WIN31\ICU} directory. Next, install the Windows 3.1 drivers and 
   utilities the {\WIN31\DRIVER} directory on the same CD.

   To install the Aztech PnP Configuration Software, select File\Run option 
   from Windows pull down menu and type {D:\WIN31\ICU\SETUP}.
   
   Likewise, to install Windows 31 driver, select File\Run option from Windows
   pull down menu and type {D:\WIN31\DRIVERS\SETUP}.

   Note :  letter D: in the { } represents your CDROM Drive. 



   Playback and Recording at the same time
   =======================================
   Full Duplex and Fast DMA features are disabled by default. To enable them,
   go to "Settings tab" in the "Sound, video and game controller" section 
   under Control Panel System\Device Manager utility and check the respective
   box.


   Playback of High Density Wave File
   ==================================

   Playing a high resolution and high sampled WAVE file with the WaveRider 
   Platinum Sound Driver on some machines may cause some delay in the playback.
   This is mainly due to the heavy utilisation of the system CPU resource.  
   Listed below are the workaround to these limitations. 

   1. Remove any CD in your CDR ROM Drive before playing the WAVE file.
      As the Windows driver is checking the drive frequently for the CD 
      status. (CDROM controller using EIDE interface will use up to 100%
      of CPU resource when activated).
  
   2. Disable the Software WaveTable option found under the "Settings tab"
      in the "Sound, video and game controller" section under Control Panel
      System\Device Manager utility.  This will release the CPU utilisation
      taken up by the Software Synthesis.


   Installation on Windows 95 Platform
   ===================================

   Start up Windows 95 Operating System. Windows 95 will then automatically 
   detects the AZT2320 PnP Sound Device and prompts a dialog box with the 
   option "Driver from disk provided by manufacturers" being highlighted.
   Please insert the Audio Installation Disk#1 into Drive A: (or Drive B:)
   and change the path to a:\ (or b:\) and click OK to install the
   drivers. Windows 95 will then automatically proceed to detect all the other
   logical devices. 

   Note: If you do not have Windows 95 Multimedia Applications installed
         previously, system may prompt you to complete the installation of
         the Multimedia Applications prior to the copying of the Audio Device 
         drivers. Just follow the on-screen instructions to complete the
         installation of Multimedia Application and AZT2320 PnP Sound Drivers.
         
   Next, please proceed to run 'A:\SETUP.EXE' from the Installation Disk #1, 
   a program group will be created with this README.TXT included.

   You might encounter some resource conflicts after loading the PnP 
   devices (especially when there are non-Plug & Play adaptors installed in 
   your system). Please refer to Trouble-shooting section in Windows 95 for 
   further details.


   Cards with 3D function
   ======================

   For Windows 95, the mixer can be found under the group name formed after
   installation. This is in turn located under 'Programs' in the 'Start' menu.
   The '3D' function can also be activated through the Microsoft Volume Control
   Panel.  This can be done by clicking on the default Microsoft 'Speaker' icon
   located at the bottom right corner of the screen.  Choose 'Options' and then
   'Advanced Controls' from menu.  Click on the 'Advanced' button and the 3D
   sound effects can be chosen. 




   
        ***********************************************************
        *  In case you encounter any problem with our products,   *
        *  please quote the following model(s) when calling our   *
        *  Technical Support :                                    *
        *                                  Egret96 Sound Card     *
        *********************************************************** 





                         -------  The End  ---------


