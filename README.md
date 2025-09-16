![Workshop_header_template](/Workshop_header_template.png)
# Welcome to the Total War: Empire Mobile Modding Tools GitHub
Welcome! This is the home of the Total War: Empire mobile modding tools and documentation. This is the main place to access the official tools required to get you started.

# Table Of Contents

* [Important Information](#important-information)
* [Documentation](#documentation)
  * [Mod Location](#mod-location)
     * [iOS Mod Location](#ios-mod-location)
     * [Android Mod Location](#android-mod-location)
  * [Mod Commands File](#mod-commands-file)
  * [Mod Logs File](#mod-logs-file)
  * [Mobile Packs](#mobile-packs)
  * [Example Mod](#example-mod)
* [Rules](#rules)

# Important Information

Modding the game can cause crashes and other issues especially if your phone hardware cannot support the additional or larger assets used in some mods. feral only offer support for playing the game un-modded. For any modding issues you should contact the team that made the mod you are trying to play.

Modding requires ownership of the base game and the "A New World" expansion.

Modding works on iOS and Android however on Android you will need to use a File Manager that grants you access to the Empire data area.

# Documentation

## Mod Location

These folders will only work if you own the A New World expansion.

### iOS Mod Location

Open the "Files" appliction and go to the "On My Phone" section, then select "Empire Total War", then open the folder called "FeralEmpireMods". All mods and launch options will be placed inside this folder.

### Android Mod Location

To access the files on Android you will need to use a file manager that will give you access to the data section of your Android phone. This will be slightly different depending on your phone and the exact methods are beyond thew scope of this page.

You can find the Empire mod folder at the following path:

`Android/data/com.feralinteractive.empire_android/files/Documents/FeralEmpireMods`

##  Mod Commands File

This file is used to tell the game what mod files to load, it also can be used to pack and unpack data files and extract strings from the game. Each command needs to be on it's own line and end with the `;` symbol. You can leave comments using the `//` at the start of the line. 

Valid commands include:

* `unpack` - This will unpack a valid pack file into the modding folder. You can reference any pack from the base game or even a pack file inside the modding folder. This is similar to packing tools on the desktop but supports the additional compression used on mobile.
  * Example `unpack models_1.pack;`
* `pack` - This will pack a folder into a pack file that then can be loaded in a mod.
  * Example `pack example_mod.pack;`
* `generate_strings` - This command will export all the strings for the game into a text file.
  * The file will be called `strings.txt` inside the `FeralEmpireMods` folder.
* `mod_strings` - This allows you to load custom strings for a mod. Please note you only need to include modified strings any strings that are not modified should NOT be included to improve performance and make it easier.
  * Example `mod_strings example_strings.txt;`
* `grab_misc` - This command exports some loose files so they can be modded if needed. You need to include the modded files inside a pack file for them to be used in a mod. You need to match the folder structure in a similar way to other pack file structures.
  * The folder will be called `misc_data` inside the `FeralEmpireMods` folder.
  
## Mod Logs File

When running the `mod_commands.txt` file a new file will be created called `mod_logs.txt` inside the `FeralEmpireMods` folder. This will report some basic loading information for the mod confirming the commands that are being run while the mod loads. Please note it will not contain and details after the mod files are loaded.

## Mobile Packs

The mobile version has some addional data packs compared to the desktop version. This page contains a list of all the packs the mobile version uses. The addional packs are linked to some of the mobile based features, in most cases the pack name will explain what the items in the pack are focused on.

[Pack Files](/Pack_Files.md)

## Example Mod

To help show how modding should work we have created the following example mod. This mod will unlock the pirate faction as a playable faction and adds in one new unit (complete with new strings).

[Example Mod](/Example_Mod.md)

# Rules

* We welcome pull requests with improvements to the tools or documentation
* Bugs logged here should **ONLY** relate to modding questions.
