# ratchetps2rando
[![Discord](https://discordapp.com/api/guilds/951548841310695425/embed.png?style=shield)](https://discord.gg/33KUTCWH)

## Installation

- Open the seed generator [seed generator](https://champthehippie.github.io/ratchetps2rando/Randomizer_code_without_logic)
- Enter a seed number (or leave blank for a random seed), and then press `Randomize`.
- Once the seed is generated, press `Save Cheat File` which will save a `.pnach` file to your downloads folder
- Move this file to your Emulator's cheat folder and enable cheats in the emulator settings.
- Load PAL v2.0 of Ratchet & Clank and a save file to play.

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