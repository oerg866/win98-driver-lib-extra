=======================================================================
AU8830 Windows 9x Driver                                     README.TXT
=======================================================================
This is the Vortex AU8830 Windows 9x driver version 4.06.2031

CONTENTS
 I.  Overview
       A.  Windows 9x system requirements
       B.  New features
 II. Quick start
III. Software Installation
       A.  Driver installation
       B.  DirectX installation
       C.  Uninstalling the drivers
 IV. Legacy audio compatibility
       A.  Checking your hardware configuration
       B.  Changing the hardware configuration
       C.  DOS Boxes
       D.  Real-mode DOS
       E.  Compatibility List

=======================================================================
I.  Overview
=======================================================================

A. WINDOWS 9x SYSTEM REQUIREMENTS:

   * 100MHz Pentium-compatible CPU.
   * 16MB DRAM (the Vortex hardware wavetable engine uses a native
     4MB sample set. Samples are stored on disk and swapped to RAM
     as required. Typical DRAM footprint is <2MB.
   * 15MB hard disk space
   * CD-ROM drive
   * Access to Microsoft Windows 9x Installation CD-ROM.
   * Good-quality speakers or headphones and connecting cables. 
   * Joystick and MIDI keyboard (optional).


B.  NEW FEATURES:
     This section lists new features incorporated into the Vortex drivers.

(i) New and improved Icons on the A3D Settings test button.
(ii) Added S/PDIF 44.1kHz support on AU8830.
(iii) Updated the system tray program to reflect new output mode names: Satellite 
    speakers, Monitor Speakers and Quad Speakers.
(iv)  Added full support for SPDIF PCM support on all of the 8830 cards that 
    support SPDIF.
(v)  The user interface on the Control panel has a fader on the A3D Settings 
    page, which allows the user to Fade between the front and rear outputs. The
    fader is only functional on boards that have four outputs with speakers 
    connected to them.
(vi) Added support for a one step uninstall.
(vii) AC-3 support works through the waveout interface.
(viii) Added new A3D 2.0 Demo App : "A3D 2.0 Rooms"
(ix) Hardware Detection for Quad and Stereo Codecs.
(x) Full Quad support for all playback modes: 

    Quad support for Non 3D streams:  They are distributed equally to the front 
    and rear channels.

    Quad support for A3D:  Full A3D rendering and crosstalk on front channels 
    plus panning on the rear channels.  This includes A3D SuperQuad which is a 
    quantum leap over standard quad solution used by 4 speaker 3D audio systems 
    (discrete 4 channel panning).  Vortex 2 significantly improves upon that 
    solution by introducing A3D SuperQuad: the combination of discrete 4 channel 
    panning with HRTF support.  The result is better 3D positioning coverage for
    the locations where there are no speakers: above/below listener, in between 
    speakers, and inside / outside of the circle formed by speakers.

    Quad support for DS3D: Full rendering on front channels plus panning 
    on the rear channels.

(xi) Selection between Narrow and Wide speaker placement for A3D.
(xii) Support for multichannel AC-3 playback was added through the waveout interface.
(xiii) Added support for additional Codecs.

C.  WINDOWS 9x DRIVER ISSUES:

(i) Joystick Acceleration - Windows 9x always uses the standard analog
  gameport by default. Use the Gameport control panel's "Advanced" tab
  to select the Vortex gameport driver for a boost in speed.
(ii) Multiple sound cards - Some sound cards, such as Ensoniq sound
  cards, do not correctly report their I/O port utilization to the
  operating system, which can hang the system.
(iii) Diamond Monster 3D Graphics card - Download the new drivers from
  Diamond's WWW site to fix noise problems with some games, such as
  "Incoming."
(iv) Hercules Stingray 128 Graphics Card - In the "Display Properties"
  control panel, enable "Allow PCI retries" to fix audio problems.
(v) IBM 300GL and Sony VAIO USB -  A system hang may occur during
  Vortex driver installation. Disable USB during installation to fix.
(vi) In order to disable AU30DOS.com from loading into memory on your 
  system for Real-Mode Dos, you must place a REM in front of the line
  in your autoexec.bat so that it looks like this:

  REM LH C:\WINDOWS\AU30DOS.COM

  Deleting the au30dos.com line in your autoexec.bat will not work
  because the system registry will add the line back if it is not
  present.
(vii) Disabling "Sound Blaster Pro Emulation" in the device manager of
  Windows 95/98, will also disable Real-Mode Dos support which prevents
  AU30DOS.com from loading into memory.



=======================================================================
II.  Quick Start
=======================================================================

   1.  Remove any existing Vortex drivers from previous installations.
   2.  Install the Vortex hardware.
   3.  Install the Vortex Windows 9x drivers, Microsoft DirectX 6.0,
       and Vortex demonstration applications.


=======================================================================
III. Software Installation
=======================================================================

A. DRIVER INSTALLATION 

   If you have older drivers in your system, please uninstall them
   first, as described in Section C below.
   1.  Power on the system, placing the Install CDROM in the
       CDROM drive.
   2.  Windows 9x displays "New Hardware Found" message and starts
       driver installation.
   3.  If Windows prompts you to provide the drivers for the PCI
       multimedia audio device, choose "Driver Disk Provided by
       Manufacturer" and select the installation CD-ROM's root 
       ("\Win9x\<Language Desired>") directory.
   4.  You may also be asked to insert the Windows 9x CD-ROM during
       the install process.

   Note: Some Windows 9x versions (OSR2) do not show this prompt.
   Instead, they ask whether to search the diskette and CD-ROM drives
   for the appropriate drivers.

   Installed drivers may include Vortex PCI audio, Vortex wavetable,
   Vortex mixer, DOS modem port, Vortex gameport interface, Vortex
   MPU401 interface, and Vortex Sound Blaster emulation.

   Depending on the version of Windows 9x and the configuration of the
   system, you may be prompted to provide several file locations. Here
   are the CD-ROMs and directory locations for which you may be
   prompted:

        Vortex Installation & Driver Disk   \Win9x\<Language Desired>
        Windows 9x Installation Disk        \Win9x\<Language Desired>
        Microsoft DirectX 6.0               \Directx
        Vortex Application Setup            \A3DDemos
        PCI Multifunction Audio Device      \Win9x\<Language Desired>

   You may be asked to reboot several times during installation.
   Reboot when asked.  Additional software will continue to load when
   Windows restarts, until all components have been installed.

B. DIRECTX 6.0 INSTALLATION

   In most cases, Vortex installs DirectX 6.0 automatically. If you
   have an unusual system configuration , you may be prompted to
   install Microsoft DirectX 6.0 after Vortex driver installation.
   1.  When the DirectX setup panel opens, select "Reinstall
       DirectX". (Even if you do not have DirectX installed on
       your machine, the Microsoft DirectX 6.0 setup program still
       asks if you wish to reinstall).
   2.  You may receive some prompts as to whether to replace specific
       DirectX files on your computer. If you've previously installed
       an older version of DirectX on your machine, be sure to replace
       any sound-related DirectX drivers. Video DirectX drivers do not
       need to be changed.

C.  UNINSTALLING THE DRIVERS

   1.  Open the Windows 9x control panel's "Add/Remove Programs"
       applet.
   2.  To remove the drivers, double-click "Aureal Vortex". A
       Vortex uninstaller application starts.  In order for the
       Process to complete, the system needs to be rebooted.
   3.  To remove the demo applications, double-click "Aureal
       Vortex Applications". There is no need to reboot the
       computer.

=======================================================================
IV. Legacy Audio Compatibility
=======================================================================

A. CHECKING DOS AUDIO CONFIGURATION

    Be sure to configure the games for Sound Blaster Pro or Sound
    Blaster operation. Typical settings are I/O 220h, IRQ5, and DMA3.
    You can verify your system is configured for these settings the
    resource tab under:

        Control Panel->
           System (Device Manager) ->
              Sound Video, and Game Controllers->

    Available settings:
    I/O range:           220h, 240h, 260h, and 280h
    Interrupt:           5, 7, 9(2), 10
    DMA:                 1, 3
    Joystick port:       201h, 202h, 203h, 204h, 205h, 206h, and 207h.
    MIDI port:           300h, 310h, 320h, and 330h.
    Not all of these settings may be available, depending on the
    hardware in your computer.

B. CHANGING THE HARDWARE CONFIGURATION

    Generally, you should not need to change the hardware settings.
    If you wish to use manual settings, use the following procedure:
    1. Open "Sound Blaster Emulation", "Gameport Interface" or "MPU-
       401 Interface" in the system control panel's "Sound, Video
       and Game Controllers" tree.
    2. Clear the "Use Automatic Settings" checkbox.
    3. Select "Basic Configuration 0007"
       (This lets you select all possible settings on your computer.) 
    4. Move the highlight to select the resource to change.
    5. Press the "Change Setting" Button.
    6. Change settings and press "OK."
 
    When you change DOS audio settings, the drivers automatically
    update the BLASTER environment variable in your AUTOEXEC.BAT
    and DOSSTART.BAT configuration files.

C. DOS BOXES

    Windows DOS boxes are launched from the "MSDOS prompt" in the
    Windows 9x Start menu. Simply run the game as usual. The game
    still needs to be configured for the Vortex hardware settings.

    Vortex provides wavetable support in DOS boxes if the game
    supports General MIDI output. To use wavetable in a DOS box:
    1. Open the Vortex Control Panel MIDI tab.
    2. Ensure that "Vortex Wavetable Receives DOS Box MIDI" is
       selected.
    3. Open the application in a DOS box. Configure the music to use
       MPU-401 output.
    The Vortex drivers can also send MIDI to other software wavetable
    or external MIDI devices installed or attached on your computer.
 
D. REAL-MODE DOS

    DOS runs in real mode when Windows 9x is not loaded, or when you
    restart the computer in MSDOS mode from Windows 9x. In real mode,
    make sure the game is configured correctly. Select Sound Blaster
    or Sound Blaster Pro for both the Music and the Effects device
    (unlike in DOS box where you can select MIDI for Music). You can
    select MPU-401 output if you have an external synthesizer connected
    to the Vortex MIDI port. Make sure the settings for I/O, IRQ, and
    DMA match the configuration for the Vortex card.

    When you install the Vortex drivers from CD-ROM, Vortex adds some
    lines to your computer's AUTOEXEC.BAT and DOSSTART.BAT files:

       PATH=C:/WINDOWS
       AU30DOS
       SET BLASTER=A240 I5 D3 T4

    AU30DOS is the Vortex real-mode DOS driver, which is installed in
    your default Windows directory (C:\WINDOWS by default). If Vortex
    detects an upper memory manager, it attempts to load AU30DOS high
    (see your memory management documentation for more information).
    Your computer finds AU30DOS via the PATH statement, which includes
    a reference to your Windows directory. Your computer then executes
    the AU30DOS program during boot. When AU30DOS is executed, you
    see text similar to:

VORTEX DOS AUDIO DRIVER (2.002) Copyright (c) 1997-1999 Aureal Semiconductor
PCI AUDIO PRO enabled at Ports 220-22Fh, Interrupt 5, DMA 3, Joystick 201h.
  
    Some games require the "SET BLASTER" line to find the sound card
    in your system. In the above example, the BLASTER environment
    variable is set to I/O port 240h, interrupt 5, and DMA channel 3.
    The "T4" parameter sets the Type of Sound Blaster to Sound Blaster
    Pro. 

    When exiting from Windows to MS-DOS, the computer runs DOSSTART.BAT
    file in the Windows directory, in much the same way as it runs
    AUTOEXEC.BAT when you boot. Vortex thus places the AU30DOS.COM
    command and BLASTER environment variable in the DOSSTART.BAT file.
    These lines reinstall the Vortex DOS driver and reset the BLASTER
    environment variable. You do not need to run DOSSTART.BAT in Windows
    boxes.

E. COMPATIBILITY LIST

    Correct audio operation has been verified on the following games.

    * Games that run in a DOX box are flagged with and asterisk.
   ** Games that run in a DOS box, whereas the original Sound Blaster Pro
      card requires real-mode DOS, are flagged with two asterisks.


     	
        11th Hour*			Magic Carpet 2*
        1942 Pacific Airwar		Master of Orion*
        3D Labyrinth*			Master of Orion 2*
        7th Guest*			Masters of Magic**
        Absolute Zero*			Math Ace*
        Abuse*				Math Rescue*
        Aces of the Deep		MAX*
        Across the Rhine*		MDK**
        Aegis				Mech Warrior 2*
        Alien Legacy*			MegaRace*
        Alone in the Dark*		MegaRace II**
        Are you Afraid of the Dark	Metaltech Earthsiege*
        Armored Fist			Mickey's 123*
        Armored Fist 2*			Might and Magic II 
        Bailey's Bookhouse*		Might and Magic III
        Baseball 94 (FPS)		Mortal Kombat 1*
        Baseball Tonight*		Mortal Kombat 2
        BattleChess			Mortal Kombat 3
        Battledrome			MS Flight Sim 5*
        Beast Within(Gabriel 2)*	Nascar Racing
        Betrayal at Krondor*		Nascar Racing 2*
        Big Red Racing*			NBA Jam TE*
        Bioforge			NBA Live 95*
        Black Thorne *			NBA Live 97
        Blake Stone*			Need for Speed**
        Blood*				Nemesis**
        Blood Bowl			NHL Hockey 96
        Breach 3*			NHL Hockey 97**
        Brett Hull Hockey 95		Night Trap*
        Bureau 13**			Necropolis*
        Busy Town*			Orion Conspiracy*
        Caesar 2*			Out of this World
        Capture the Flag*		Pandora Directive**
        Carmageddon*			Panzer General*
        Carmen Sandiego*		PGA Tour*
        Castle of Dr Brain**		Phantasmagoria*
        Castle Wolfenstein 3D*		Piranha*
        Chaos Engine*			Police Quest 4*
        ChronoMaster*			Populous II*
        Circle of Blood*		Power F1 Racing*
        Circuit Racer*			Power Monger
        City of Lost Children*		Prince of Persia 1*
        Civilization*			Prince of Persia 2*
        Commanche Overkill		Privateer 1
        Command & Conquer*		Privateer 2
        Commander Blood			Psychic Detective
        Commander Keen 4*		Pure War Game
        Conqueror*			Quake 0.9x*
        Conspiracy*			Quake 1.0x*
        Constructor**			Railroad Tycoon*
        Corridor 7*			RAMA*
        Creature Shock*			Raptor*
        Crusader			Ravenloft*
        Cyber Mage**			Reading Carnival
        Cyberia**			Realms of the Haunting*
        CyberWar*			Rebel Assault 1
        D*				Rebel Assault 2*
        Daggerfall Chronicles**		Rebel Runner*
        Dark Forces			Red Baron*
        Dark Light Conflict**		Redneck Rampage**
        Dark Sun: Shattered Lands*	Relentless
        Day of the Tentacle*		Return to Ringworld*
        Death Gate*			Return to Zork*
        DeltaV				Ripley's Believe it 
        Descent 1*			Rise of the Triad*
        Descent 2 *			Rocketeer
        Desert Strike			Savage Warrior*
        Dig*				Scorcher*
        Doom 1*				Screamer 2*
        Doom 2*				Scud Attack*
        Dragon Lore			SDI 2040*
        Dragon's Lair			Seawolf*
        Duke Nukem 2 **			Shadow Caster 
        Duke Nukem 3d*			Shadows of Cairn
        Earth Treks*			Shadows of Riva**
        Ecstatica*			Shattered Steel**
        Epic Pinball			Silent Hunter*
        Eradicator			Silver Pinball*
        ESPN 2 Extreme Games*		SimAnt*
        Extractors*			SimCity*
        F117a Demo*			SimIsle*
        F22-Lightning 2*		Simon The Sorcerer*
        Fable*				Sunny's Back to the Forest*
        Falcon 3.0			SlipStream 5000**
        Fade to Black*			Space Quest 4*
        Fast Attack*			Space Quest 6*
        FIFA 97				Spycraft*
        Fleet Defender			Star Command*
        Flight Unlimited		Star Control 1*
        Fighter Duel			Star Control 2*
        Football Pro 95			Star Control 3*
        Football Pro 96			Star Fighter**
        Full Metal Jacket*		Star Trek: 25TH**
        Full Throttle*			Star Trek: Final Unity
        Future Shock*			Steel Panthers*
        FX Fighter**			Steel Panthers 2*
        Gabriel Knights*		Stellar 7*
        Gene Wars*			Stonekeep
        Global War*			SU 27 Flanker**
        Grand Prix II**			Super Karts*
        Great Naval Battles*		Syndicate Wars*
        Gunship 2000			System Shock*
        HardBall 3*			Table Sports 3D*
        Hardball 4**			Tank Commander
        Hardball 5*			TekWar**
        Harpoon 2*			TerraNova*
        Harpoon 2 Deluxe		Terminator 2029*
        Hell*				Test Drive Off Road*
        Heretic*			Theme Park*
        Hexen*				Thunder Strike Air Assault*
        Hi-Octane			Thunder Truck Rally
        Hind				Tie Fighter*
        Hocus Pocus			Time Treks*
        I Have No Mouth*		Tomb Raider**
        Inca				TonyLaRussa Baseball3*
        Incredible Machine*		Top Gun*
        Indiana Jones			Torin's Passage*
        IndyCar				Transport Tycoon*
        Iron Assault			TreeHouse*
        Iron Cross*			Twinson's Odyssey*
        Jack Nicklaus*			Ultima 7
        Jagged Alliance*		Ultima 8
        Jagged: Deadly Games*		Ultimate Football  95
        Jane's Adv. Fighters 		Under a Killing Moon
        Jane's Longbow*			Unnecessary Roughness*
        Jazz Jackrabbit*		Unnecessary Roughness 95*
        Jill of the Jungle*		USNF
        Jumpjet*			Vikings*
        Kid Pix*			Warcraft*
        Kids Zoo*			Warcraft 2*
        Kings Quest 5			Wetlands*
        Kings Quest 6*			Wing Commander 2
        Krush Kill & Destroy*		Wing Commander 3*
        LawnMower Man			Wing Commander 4*
        Leisure Suit Larry 5*		Wing Commander Armada
        Leisure Suit Larry 6*		Wings of Glory
        Lemmings Chronicles		Winter Sports
        Lighthouse*			Witchaven*
        Links386 Pro			Witchaven 2**
        Lord of the Realm 2*		Word City*
        Lord of the Rings*		X-Com*
        Lost Eden*			XCom Terror from Deep*
        Machiavelli the Prince		X-Wing*
        Madden 97*			XCAR*
        MadDog McCree*			Z*
        MadDog McCree 2*		Zephyr
        Magic Carpet 1*			Zone Raiders*
        				Zork Nemesis
        
(i) Autodetect
  Some older games do not detect audio hardware automatically. You
  can still use Vortex legacy audio support for these games by
  configuring the hardware resources manually:
	* Carmaggedon                   * Fast Attack
        * Castle of Doctor Brain        * Grand Prix II 
	* Command and Conquer           * Hard Ball 4
        * Constructor                   * MDK 
        * Cyberwar                      * Witchaven 2
(ii) Sound Blaster/Sound Blaster Pro Selection
    If both options are available, pick "Sound Blaster Pro" for best
    quality. The following games work if "Sound Blaster" is selected:
	* Battlechess                   * NHL Hockey 96 
	* Cyberia (use DMA1)            * NHL Hockey 97 
	* Death Gate                    * Ripper 
	* FIFA97                        * Spycraft
	* NBA Live 97 

=======================================================================
Aureal, A3D, A3D-I, A3D-Interactive, and the Aureal logo are trademarks
and Vortex is a registered trademark of Aureal Semiconductor Inc.

All other trademarks are owned by their respective owners.

(C) Aureal Semiconductor, Inc. 1996-99. All Rights Reserved.
=======================================================================
For Technical Support please contact your board manufacturer.
=======================================================================