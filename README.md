# EEUITweaks User Interface Mods Collection Version 4.0.6

The goal of EEUITweaks is to be a collection of the individual UI.MENU (i.e. Extended Edition 2.x+) mods/patches/tweaks from the BeamDog UI Modding forum; packaged as a single WeiDU collection. The advantages are to automate the tedious manual editing of UI.MENU, simplify multiple mod installations (particularly after an update), and to provide a single source from which many EE GUI mods can be accessed. It does NOT install the full UI replacement environments, although it does support modding them.

EEUITweaks supports BGEE, BG2EE, BGEE/SoD, PST:EE, IWDEE, and EET with the BG2(default) and SoD (EET_gui) user interfaces. It also supports installing mods on the Dragonspear UI++, BG2EE GUI To BGEE, LeUI, Revised Dragon Scale, IWD GUI for BG2:EE and BG:EE, and IWD2 for BG2 replacement UIs. In all cases, it will skip attempting to install useless or invalid mods for a particular environment (e.g. transparent sidebars on Dragonspear UI++).

## Installation

To install the mod:

1. Copy setup-EEUITweaks.exe and the EEUITweaks directory tree to your game
   installation directory (contains the chitin.key file)

2. Run setup-EEUITweaks.exe, answering the questions it asks.
   Depending on where your game is installed and the security settings on your
   system, you may need to 'Run as Administrator'. In fact, it's probably a
   good idea just to do it anyway.

That's it! It should install with no problems.

## Components

### Mod Options
([Original thread](https://forums.beamdog.com/discussion/59740/mod-mods-options-bg-ee-sod-and-bg2-ee-tob))

Adds screens to see the list of installed UI mods inside the game and toggle option offered by these mods.

The new list screen is accessible from both
- an "Option" button on the start screen
- an "Option" button in the game's (original) "Option" screen

From the mod list screen you can access the list of options offered by the mod (if any).

Screenshots:
- [SoD start screen](https://forums.beamdog.com/uploads/editor/bh/xgdd3mi7lw1z.png) | [SoD options screen](https://forums.beamdog.com/uploads/editor/f6/avo75x0bseci.png) | [SoD mod list screen](https://forums.beamdog.com/uploads/editor/re/u9beby5wdui3.png) | [Sod mod options screen](https://forums.beamdog.com/uploads/editor/2u/1scn6vm2ba6u.png)
- [BG2 start screen](https://forums.beamdog.com/uploads/editor/k8/ebsabpb7isrk.png) | [BG2 options screen](https://forums.beamdog.com/uploads/editor/nb/11b878t3mvhi.png) | [BG2 mod list screen](https://forums.beamdog.com/uploads/editor/lw/rx5avmgv097s.png) | [BG2 mod options screen](https://forums.beamdog.com/uploads/editor/hc/c0dfyanxbd1q.png)

### Hidden Game Options
([Original thread, same as "Mod Options"](https://forums.beamdog.com/discussion/59740/mod-mods-options-bg-ee-sod-and-bg2-ee-tob))

Uses the previous "Mod Options" UImod to give access to (vanilla) game options that are normally hidden and can only be changed by editing `baldur.lua`.

Sreenshot: [SoD "Hidden Option" mod options :p](https://forums.beamdog.com/uploads/editor/dy/lxd0kyfpgj0f.png)

### lefreut's Character Creation Screens

Takes the Character creation screens from [Lefreut's Enhanced UI](https://forums.beamdog.com/discussion/61571/mod-lefreuts-enhanced-ui-for-bg1ee-sod-bg2ee-and-eet)
> Modify the character creation screens to something closer to the v1.3 look.

Applies on **unmodified BG:EE, BG2:EE or EET** (i.e. it is not installable over any LeUI variant, dragonspear++ or IWD:EE).

There are two options for this component : "default button position" or "reversed button position".

## Mr2150's Portrait Picker
([Original thread](https://forums.beamdog.com/discussion/56916/mod-portrait-picker-for-bgee-sod-and-bg2ee-v2-1))

Portrait picker with list, sorting, filtering.
- portraits can be given a gender and description
- those can be used for sorting and filtering
It has two versions, scaled (all except BG:EE without SoD or LeUI) or non-scaled (EET or BG:EE with SoD but no LeUI/DS++).

Incompatible with [lefreut's Portrait Picker](#lefreuts-portrait-picker)

Screenshots: [SoD](https://forums.beamdog.com/uploads/editor/eb/dkto779scwa9.png) | [BG2:EE](https://forums.beamdog.com/uploads/editor/xa/0bop55y2upa8.bmp)

## lefreut's Portrait Picker

Takes the Portrait picker screens from [Lefreut's Enhanced UI](https://forums.beamdog.com/discussion/61571/mod-lefreuts-enhanced-ui-for-bg1ee-sod-bg2ee-and-eet)

EE games without LeUI or Dragonspear++.

<details>
<summary>Portrait list generation - <em>click to show</em></summary>
   
- uses portraits in `$USER_DIRECTORY/portraits`
- `$USER_DIRECTORY` depends on the OS
    * `{user personal directory}/{game name}` on Windows
    * `$HOME/.local/share/{game name}` on Linux
    * `$HOME/Documents/{game name}` on Macos
- `{game name}` is for example `Baldur's Gate - Enhanced Edition` for BG:EE or `Baldur's Gate - Enhanced Edition Trilogy` for EET
  
- list all `.bmp` files with a base name of 7 characters or less
- there are 4 genders, M, F, Z and D
   * if the filename starts with `M#` or `m#` it is added to the M list
   * if the filename starts with `F#` or `f#` then it's added to the F list
   * any other is added to the D list
   * the Z list isspecial and contains the "no portrait" portrait

The `m_nicks.lua` is static and contains descriptions/nicks for the base game portraits (but can be edited by hand... or by other mods).

</details>

Incompatible with [Mr2150's Portrait Picker](#mr2150s-portrait-picker-original-thread)

[Screenshot](https://forums.beamdog.com/uploads/editor/le/8p2r9yos0j2f.jpg)

## Mr2150's Backup M_BG.lua
Uh! no idea... Probably to recover when your M_BG.lua os broken.

Saves the `M_BG.lua` file to `override/backup-M_BG`.

Depends on [Mr2150's Portrait Picker](#mr2150s-portrait-picker-original-thread)

## Mr2150's Update Portraits

(Note: Those are speculations)
Regenerates the list of portraits for [Mr2150's Portrait Picker](#mr2150s-portrait-picker-original-thread).
Can be used after editing `M_BG.lua` and `m_nicks.lua`.
Depends on [Mr2150's Portrait Picker](#mr2150s-portrait-picker-original-thread)

## Adul's Unhide Chargen Options
([Original thread](https://forums.beamdog.com/discussion/59647/mod-unhide-chargen-options))

> The EE 2.0 update brought with it the new practice of hiding unavailable character choices during character creation. This means, for instance, that if you choose the halfling race, in class selection you will only see the 4 classes that are available to you and none of the disabled options, where in previous game versions you could see all the disabled options.

The following previously hidden options are restored:

- Classes excluded by your race selection
- Kits excluded by your race selection
- Alignments excluded by your class/kit selections
- Weapon proficiencies excluded by your class/kit selections

Incompatible with [lefreut's Portrait Picker](#lefreuts-portrait-picker), [lefreut's Character Creation Screens](#lefreuts-character-creation-screens) and  DragonspearUI++.

## Faydark's Abilities Auto-Roller/GrimLefourbe's BG2 UI
([Original thread](https://forums.beamdog.com/discussion/51777/mod-bg-ee-chargen-abilities-screen-show-stored-values-and-simple-auto-roller/p1))

1. When storing a set of abiliy rolls, you can see it while you continue rolling side by side with your current rolls
2. Adds an "Autoroll" button that keeps rolling (until you tell it to stop) and stores the biggest value

[Screenshot](https://forums.beamdog.com/uploads/editor/i4/ofbin5zkcjp8.png)

Incompatible with [Mr2150's Roll First](#mr2150s-roll-first) and DragonspearUI++.

## Mr2150's Roll First
([Original thread](https://forums.beamdog.com/discussion/59780/mod-roll-first-beta-for-bgee-sod-v2-2))

Adds a "Roll first" button at the start of character creation for an alternate character creation. The abilities are rolled before you choose the race and class. You can then "fix" the abilities to match the race/class requirements.

Incompatible with [Faydark's Abilities Auto-Roller/GrimLefourbe's BG2 UI](#faydarks-abilities-auto-rollergrimlefourbes-bg2-ui) and Random PC generator

## Display max proficiency limits

Shows how many points can be put in a proficiency, even if they are not available because the character is limited by their level.
