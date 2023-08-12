# RAC1 PS2 Randomizer v0.1.1
[![Discord](https://discordapp.com/api/guilds/951548841310695425/embed.png?style=shield)](https://discord.gg/33KUTCWH)

## Introduction

This is an early build for a Ratchet & Clank (PS2) randomizer, it works using gameshark codes and a pre prepared save file.

- Start on Veldin 2
- You have no items
- All planets are open
  - Except Orxon and Gemlik base which are unlocked when O2 mask is found
- Items are located on Gold Bolts
- Golden Weapons are progressive
 - There are 2 copies of the item in the pool:
  - Collecting the first one gives you the normal weapon
  - Collecting two gives you the gold version
- Collecting a pack gives you clank

Known Bugs:
- Items can still be purchased:
 - Al sells the helipack
- You can easily get stuck in a location, save and then load the file to return to your ship
- No logic is present, most seeds will not be beatable
- Many items are not present in the item pool:
 - Metal Detector
 - Raritanium
 - Hoverboard
 - Bolt Grabber
 - Persuader
 - Platinum Zoomerator

## Installation

- Open the seed generator [seed generator](https://champthehippie.github.io/ratchetps2rando/Randomizer_code_without_logic)
- Enter a seed number (or leave blank for a random seed), and then press `Randomize`.
- Once the seed is generated, press `Save Cheat File` which will save a `76F724A3.pnach` file to your downloads folder.
 - (Optional) press `Save Spoiler Log` to save a .txt file that will list all randomized locations and what items they contain.
 
### for PCSX2 (Emulator running on PC)
 
- Move the `76F724A3.pnach` file to your PCSX2 `cheats` folder.
 - Make sure you are using PCSX2 Nightly build v1.7.xxxx or later.
- Move [this](https://drive.google.com/file/d/1XvIiDHySYcOxELpgGW-PmfRw5Xau7koE/view?usp=sharing) save file into the `memcards` folder.
- Start PCSX2, go to Settings > Memory Cards, right click `RatchetRando.ps2` and select `Use for port 1`.
- Open the `Emulator Settings` page, select `Enable Cheats` under system settings.
- Start your game (PAL v2.0) and then select any of the save files from the main menu.

### for OPL (PS2 Homebrew)

- not currently compatable with this version

## Web page functionality

- Seed Number Box: A textbox to enter the seed number you wish to use to generate a randomization
- Randomize: Generates a randomization using the entered seed value, the same number gives the same randomization every time, leave blank to use a random seed.
Once generation has completed then the generated seed number used is displayed along with 2 buttons:
- Save Cheat File: Downloads a .pnach file that contains the cheatcodes used for randomizing the game.
- Save Spoiler Log: Downloads a .txt file that lists the locations and what items are shuffled to those locations.

## Shuffler functionality

- PRNG function: Uses a stable random function to give the same item placements given the same seed value used.
- Cheat File Generator: The text that is printed to the .pnach is dynamically generated, allowing for different options/settings to choose what gets randomized.
- Spoiler Log Generator: Generates a spoiler log given the item and locations, sorts the entries into location order to match the standard set by other randomizers spoiler logs.

## To Do

- Logic: Add logic conditions to each location, create a function to evaluate if the proposed shuffle step is valid based on these conditions.
- Debugging: Throw errors where things can go wrong and print them to a log, allow the user to download the log file to submit in a bug report.
- Starting Items Setting: Allow the user to select which items should be added at the start of the game, create a bolt pack item to act as junk filler.
- Skill points setting: Add shuffle locations for each skill point.
- Refactor: Everything is in one file but should be split up in an appropriate file convention.