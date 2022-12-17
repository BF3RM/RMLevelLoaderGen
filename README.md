# RMLevelLoaderGen

Contains all files required by [LevelLoaderGen](https://github.com/BF3RM/LevelLoaderGen) to generate our custom level loader mod.

## Pre-requisites

- [Python](https://www.python.org/downloads/)

## Installation

Clone this repo **outside** your mods folder as this repository should not be confused with a Venice Unleashed mod. It generates a Venice Unleashed mod!
Instead clone it in e.g. `Documents/Projects` instead.

## Usage

Save files generated with [MapEditor](https://github.com/BF3RM/MapEditor) can be placed in the `in/map_saves` folder. The files should have a `.json` extension, the file names themselves don't matter.

Once done with map modifications, simply run the `generate.bat` file. This will generate a new version of the mod. The mod can be found in the `mods/rm-levelloader` folder. Copy this folder to your `Server/Admin/Mods` folder and enable it in the `ModList.txt`.

### Extract to Mods folder

The [LevelLoaderGen](https://github.com/BF3RM/LevelLoaderGen) has support for different output paths, so you can set it up to directly copy the generated mod to your `Server/Admin/Mods` folder. To do this, make a copy of the existing [generate.bat](./generate.bat) file and place it somewhere where you can find it back. After that you should make sure that the path to LevelLoaderGen is correct and add an extra flag like shown below:

```bat
@echo off
cd <path_to_rmlevelloader>
call ./LevelLoaderGen/bin/levelloader-gen rm-levelloader 0.2.0 -i ./in -o "<path_to_documents_bf3>/Server/Admin/Mods"

pause
```
