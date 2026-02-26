🎮 Phantom Menace PC – Core Patch

Modern Engine Fixes, FOV System & 60 FPS Mod

created and maintained by Chip

Reverse Engineering • Engine Research • Patching • Preservation

------------------------------------------------------------------------

About This Project

This project provides a core engine patch for Star Wars: Episode I – The
Phantom Menace (PC).

It focuses on: - Reverse-engineered engine fixes - Runtime patching -
Gameplay improvements - Modern system compatibility - Preservation of
the original PC version

This release contains only Chip’s patches. Third-party tools are not
bundled and must be downloaded from their original authors.

------------------------------------------------------------------------

Legal Notice

You must legally own an original retail copy of the game.

This patch: - does NOT include game data - does NOT distribute
copyrighted assets - modifies the game at runtime only

------------------------------------------------------------------------

What This Patch Does

-   60 FPS modification (original game is 30 FPS) Elisha wrapper should be used to make this fully stable.
-   Runtime FOV system
-   Engine timing fixes
-   Stability adjustments
-   Modern Windows compatibility improvements

------------------------------------------------------------------------

Requirements

Requires Ultimate ASI Loader.

Download: https://github.com/ThirteenAG/Ultimate-ASI-Loader

Rename: dinput8.dll → DINPUT.dll

Place DINPUT.dll next to WMAIN.exe.

------------------------------------------------------------------------

Installation

1.  Extract this release
2.  Copy the scripts folder into the game directory
3.  Launch using WMAIN.exe

------------------------------------------------------------------------

FOV System

Default hotkey: F1

Change in scripts/chip.ini

To apply changes: 1. Press hotkey 2. Press ESC 3. Close menu

------------------------------------------------------------------------

Optional Enhancements (Not Included)

Graphics — dxwrapper https://github.com/elishacloud/dxwrapper

Resolution — LegacyD3D
https://github.com/UCyborg/LegacyD3DResolutionHack

Audio — DSOAL https://github.com/kcat/dsoal

Controller — Xidi https://github.com/samuelgr/Xidi

------------------------------------------------------------------------

Modding Community

https://discord.gg/KX7R4quSQw

Reverse engineers and contributors welcome.

------------------------------------------------------------------------

Source Code Status

Closed source during active reverse engineering. Planned for release
once systems stabilise.

------------------------------------------------------------------------

Credits

UCyborg — Legacy D3D Resolution Hack
ThirteenAG — Ultimate ASI Loader
elishacloud — dxwrapper
kcat — DSOAL
samuelgr — Xidi

------------------------------------------------------------------------

Chip Reverse engineer • Programmer • Developer • Preservationist
