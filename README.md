![Workshop_header_template](/Workshop_header_template.png)
# Welcome to the Total War: Empire Mobile Modding Tools GitHub
Welcome! This is the home of the Total War: Empire mobile modding tools and documentation. This is the main place to access the official tools required to get you started.

# Table Of Contents

* [Important Information](#important-information)
* [Documentation](#documentation)
   * [Mod Location](#mod-location)
     * [iOS Mod Location](#ios-mod-location)
     * [Android Mod Location](#android-mod-location)
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

Android

##  Mod Commands File

This file is used to tell the game what mod files to load, it also can be used to pack and unpack data files and extract strings from the game. Each command needs to be on it's own line and end with the `;` symbol. You can leave comments using the `//` at the start of the line. 

Valid commands include:

• `unpack` - This will unpack a valid pack file into the modding folder. You can reference any pack from the base game or even a pack file inside the modding folder. This is similar to packing tools on the desktop but supports the additional compression used on mobile.
  • Example `unpack models_1.pack;`
• `pack` - This will pack a folder into a pack file that then can be loaded in a mod.
  • Example `pack example_mod.pack;`
  
## Mod Logs File

[Extra Docs](/Example.md)

# Rules

* We welcome pull requests with improvements to the tools or documentation
* Bugs logged here should **ONLY** relate to modding questions.
