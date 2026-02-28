<div align="center">

# 🎮 Game Specific Patches & DLL Wrappers  

***created and maintained by***

[![Chip-Biscuit Website](https://img.shields.io/badge/Chip--Biscuit-Website-blue?style=for-the-badge)](https://chip-biscuit.github.io/)

Reverse Engineering • Programming • Patching • Game Improvements • DLL Creation 

[![Total Downloads](https://img.shields.io/github/downloads/Chip-Biscuit/Star-Wars-Episode-I-Phantom-Menace-PC-Stand-Alone-Fix-Files/total?label=Total%20Downloads&style=for-the-badge)](https://github.com/Chip-Biscuit/Star-Wars-Episode-I-Phantom-Menace-PC-Stand-Alone-Fix-Files/releases/tag/PhantomAlone)

<sub>click the Total Downloads button above to take you to the releases page with the instructions and download [scripts.zip](https://github.com/Chip-Biscuit/Star-Wars-Episode-I-Phantom-Menace-PC-Stand-Alone-Fix-Files/releases/download/PhantomAlone/scripts.zip) at the bottom  of the page</sub>

</div>

# Phantom Menace PC – Core Patch
## Modern Engine Fixes, FOV System & 60 FPS Mod

------------------------------------------------------------------------

# ABOUT THIS PROJECT

This project provides a core engine patch for
Star Wars: Episode I – The Phantom Menace (PC).

Focus:
- Reverse-engineered engine fixes
- Runtime patching
- Gameplay improvements
- Modern compatibility
- Preservation of the original PC version

This release contains ONLY Chip’s patches.

Third-party tools are required and must be installed separately.

------------------------------------------------------------------------

# LEGAL NOTICE

You must legally own an original retail copy of the game.

This patch:
- does NOT include game data
- does NOT distribute copyrighted assets
- modifies the game at runtime only

------------------------------------------------------------------------

# 64-Bit Installer (Recommended – Easiest Method)

**If you want the simplest and most reliable way to install the game on a modern system, I strongly recommend using my custom 64-bit installer.**

The original 16-bit installer does not work on current versions of Windows. This installer replaces it completely and automates the entire setup process.

1. Installation is straightforward:
3. Mount the original game disc (or insert the CD).
5. Run the installer.
7. Choose your installation options.
8. Set your desired resolution in obi.ini.
9. Launch the game.
10. That’s it.

**No manual file copying, no registry edits, no compatibility tweaks.**

The installer automatically:

- Configures modern compatibility settings
- Enables DPI awareness
- Applies recommended in-game controller settings
- Handles EAX configuration (if installed)
- Applies additional stability adjustments
- Prepares the game for modern resolutions and 60 FPS support

The goal is to make the game install and run properly on Windows 10 and Windows 11 with minimal effort required.

GitHub Repository:
https://github.com/Chip-Biscuit/Star-Wars-Episode-I-Phantom-Menace-PC-64bit-Installer

------------------------------------------------------------------------

# MODDING COMMUNITY

Join the Phantom Menace reverse-engineering community:

https://discord.gg/KX7R4quSQw

Goals:
- engine research
- reverse engineering
- mod tool development
- maps, textures and models
- long-term preservation

Reverse engineers and programmers welcome.

---

# WHAT THIS PATCH DOES

Core engine improvements:

- 60 FPS modification (original game is 30 FPS)
- Runtime FOV toggle system
- Engine timing fixes
- Stability adjustments
- Modern Windows compatibility improvements

IMPORTANT:

DXWrapper is strongly recommended for stable frame pacing and smooth
performance when using the 60 FPS patch.

------------------------------------------------------------------------

# REQUIRED INSTALLATION ORDER

Install components in this order.

------------------------------------------------------------------------

# 1) ThirteenAG — Ultimate ASI Loader (REQUIRED)

Required to load the core patch.

Download:
https://github.com/ThirteenAG/Ultimate-ASI-Loader

Steps:


1. Go to the website above navigate to the releases page download (Ultimate-ASI-Loader.zip)
2. Extract archive
3. Locate:
   dinput8.dll
4. Rename:
   dinput8.dll → DINPUT.dll
5. Copy DINPUT.dll into the game directory (next to WMAIN.exe)

------------------------------------------------------------------------

# 2) Chip Core Patch

1. Extract this release
2. Copy the "scripts" folder into the game directory
3. Launch using WMAIN.exe

The patch loads automatically at runtime.

------------------------------------------------------------------------

# 3) elishacloud — DXWrapper (REQUIRED FOR STABLE 60 FPS and error "could not initialize graphics hardware" on AMD graphics)

DXWrapper provides:

- Stable frame pacing for the 60 FPS patch
- Anti-aliasing
- Anisotropic filtering
- Borderless fullscreen mode
- Modern GPU compatibility (AMD / NVIDIA / Intel)
- And much more

Download:
https://github.com/elishacloud/dxwrapper

INSTALLATION

1. Go to the releases page
2. Download the archive (dx7.games.zip)
3. Extract the archive
4. Copy the following files into the game directory
   (next to WMAIN.exe):

   ddraw.dll
   dxwrapper.dll
   dxwrapper.ini

5. Open dxwrapper.ini in a text editor.
6. Locate the [d3d9] section.
7. Ensure it is configured exactly as follows:
```
[d3d9]
AnisotropicFiltering       = 1
AntiAliasing               = 1
EnableMultisamplingATOC    = 0
EnvironmentCubeMapFix      = 0
DepthBiasFactor            = 0
DepthBiasDropOffValue      = 0
EnableVSync                = 0
ForceVsyncMode             = 0
ShowFPSCounter             = 0
OverrideRefreshRate        = 0
LimitDisplayModeCount      = 0
CustomDisplayWidth         = 0
CustomDisplayHeight        = 0
LimitPerFrameFPS           = 0
EnableWindowMode           = 0
WindowModeBorder           = 0
WindowModeGammaShader      = 0
SetInitialWindowPosition   = 0
InitialWindowPositionLeft  = 0
InitialWindowPositionTop   = 0
FullscreenWindowMode       = 1
ForceExclusiveFullscreen   = 0
ForceMixedVertexProcessing = 0
ForceSystemMemVertexCache  = 0
UseShadowBackbuffer        = 0
OverrideStencilFormat      = 0
FlipEx                     = 0
SetSwapEffectShim          = 0
DisableMaxWindowedMode     = 0
GraphicsHybridAdapter      = 0
```
6. Save the file.
7. Launch the game.

IMPORTANT NOTES

- FullscreenWindowMode = 1 enables borderless fullscreen.
- AntiAliasing and AnisotropicFiltering improve visual quality.
- VSync is disabled to prevent timing conflicts with the 60 FPS patch.

DXWrapper is considered part of the modern configuration
for stable performance.

# Alternative Option: dgVoodoo2

dgVoodoo2 is a widely used DirectX wrapper capable of translating older DirectX versions (including DirectX 7) to modern APIs such as DirectX 11 and many more options.

Download:
https://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/

**Recommended version: dgVoodoo v2.86.5 (Regular usage build)**

dgVoodoo2 may work well for some systems and is a valid alternative to DXWrapper.

It also does adress "could not initialize graphics hardware" on AMD graphics the same as DXWrapper.

**However, during my own testing:**

DXWrapper provided more stable frame pacing with the 60 FPS patch

I encountered fewer rendering issues

Because of this, the guide above is written specifically around DXWrapper. However the choice is entirely in the users hands.

**Important:**

Do not use dgVoodoo2 and DXWrapper together.

**Choose one wrapper only.**

If dgVoodoo works better on your system, feel free to use it.

Performance may vary depending on GPU, driver version, and system configuration.

------------------------------------------------------------------------

# 4) UCyborg — Legacy D3D Resolution Hack (REQUIRED for resolutions above 1920×1080)

Download:
https://github.com/UCyborg/LegacyD3DResolutionHack

Steps:

1. Extract archive
2. Copy into game directory:
   d3dim.dll
   d3dim700.dll
   obi.ini
3. Edit obi.ini to configure resolution

------------------------------------------------------------------------

# 5) kcat — DSOAL (OPTIONAL)

Restores EAX environmental audio on modern Windows.

Download:
https://github.com/kcat/dsoal

Steps:

1. Extract archive
2. Navigate to:
   DSOAL+HRTF → win32
3. Copy ALL contents into the game directory
4. Launch game
5. Enable EAX in sound settings in game

------------------------------------------------------------------------

# 6) samuelgr — Xidi (RECOMMENDED)

Provides modern XInput controller support and remapping.

Download:
https://github.com/samuelgr/Xidi

The game is 32-bit. Do NOT use the x64 version.

# STANDARD INSTALL

1. Extract the Xidi archive.
2. Open the "Win32" folder.
3. Copy:

   winmm.dll

   into the game directory (next to WMAIN.exe).

4. Create a new text file in the game directory.
5. Rename it to:

   Xidi.ini

   (Ensure it is not saved as Xidi.ini.txt)

6. Open Xidi.ini and paste the following:
```
[Mapper]
Type                = PhantomMenace

[CustomMapper:PhantomMenace]
StickLeftX          = Axis(X)
StickLeftY          = Axis(Y)
StickRightX         = Split( Compound( Keyboard(LAlt), Keyboard(RIGHT) ), Compound( Keyboard(LAlt), Keyboard(LEFT) ) )
StickRightY         = null
ButtonA             = Button(1)
ButtonB             = Button(2)
ButtonX             = Button(3)
ButtonY             = Button(4)
ButtonLB            = Button(5)
ButtonRB            = Button(6)
TriggerLT           = Button(7)
TriggerRT           = Button(8)
ButtonBack          = Keyboard(F1)
ButtonStart         = Keyboard(ESCAPE)
ButtonLS            = Button(11)
ButtonRS            = Button(12)
DpadUp              = Pov(Up)
DpadDown            = Pov(Down)
DpadLeft            = Pov(Left)
DpadRight           = Pov(Right)
```
7. Save the file.
11. Launch the game.

# FALLBACK METHOD (Some Systems)

If controller fails to initialise:

1. Rename:
   winmm.dll → winm2.dll

2. Open WMAIN.exe in a hex editor.

3. Search:
   winmm.dll

4. Replace with:
   winm2.dll

IMPORTANT:
Do NOT change string length.
It must remain 8 characters.

5. Save file.
6. Ensure winm2.dll and Xidi.ini are in the game directory.
7. Launch game.

# Controller Notes:

- Start opens the in-game menu.
- roll on right analogue stick as in the ps1 version
- Back toggles FOV (mapped to F1).
- If you change the FOV hotkey inside scripts/chip.ini,
  you must update ButtonBack inside Xidi.ini to match.
------------------------------------------------------------------------

# 7) Launching the Game

Play the game using the WMAIN.exe or make a shorcut to WMAIN.exe on your desktop.

------------------------------------------------------------------------
# FOV SYSTEM

Default hotkey: F1

To apply FOV changes:

1. Press FOV hotkey
2. Press ESC
3. Close menu

FOV updates after camera refresh.

Before level transitions:
- revert to original FOV
- allow level load
- reapply custom FOV after gameplay resumes

------------------------------------------------------------------------

# SOURCE CODE STATUS

Currently closed source.

Reason:
Active reverse engineering in progress.

Source code will release once:
- engine systems are fully mapped
- patch framework stabilises
- documentation is complete

------------------------------------------------------------------------

# CREDITS

UCyborg — Legacy D3D Resolution Hack
https://github.com/UCyborg/LegacyD3DResolutionHack

ThirteenAG — Ultimate ASI Loader
https://github.com/ThirteenAG/Ultimate-ASI-Loader

elishacloud — DXWrapper
https://github.com/elishacloud/dxwrapper

kcat — DSOAL
https://github.com/kcat/dsoal

samuelgr — Xidi
https://github.com/samuelgr/Xidi

Chip — Reverse engineering, engine patching, preservation framework
https://github.com/Chip-Biscuit

---

### Project Direction & Integration

Installer rebuild, engine research, patch integration, FOV system, FPS modifications, controller bindings, and modernisation framework:

**Chip**
“Creating compatibility fixes and enhancements for legacy PC games.”

# Chip
- reverse engineer
- programmer
- developer
- Game Preservationist
  
<img width="250" height="500" alt="my logoo" src="https://github.com/user-attachments/assets/9bb13d3f-0734-4f1d-b68f-14114b13744a" />
