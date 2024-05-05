![Mob Attack Tool Version](https://img.shields.io/badge/dynamic/json.svg?url=https%3A%2F%2Fraw.githubusercontent.com%2Fdaft-develop%2Fmob-attack-tool%2Fmaster%2Fmodule.json&label=Module%20Version&query=$.version&colorB=blue)
![Foundry Core Compatible Version](https://img.shields.io/badge/dynamic/json.svg?url=https%3A%2F%2Fraw.githubusercontent.com%2Fdaft-develop%2Fmob-attack-tool%2Fmaster%2Fmodule.json&label=Foundry%20Version&query=$.compatibility.verified&colorB=orange) ![Latest Release Download Count](https://img.shields.io/github/downloads/daft-develop/mob-attack-tool/latest/module.zip)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/S6S7XR3FZ)

# Mob Attack Tool

This is a Foundry VTT module that streamlines mob attacks in the dnd5e system. It focuses on helping the GM and players quickly resolve multiple attack and damage rolls from groups of monsters (mobs), summons, and/or creatures with the multiattack action. This module supports use of the [Dice so Nice!](https://gitlab.com/riccisi/foundryvtt-dice-so-nice/-/tree/master), [Midi-QOL](https://gitlab.com/tposney/midi-qol/-/tree/master), and [Automated Animations](https://github.com/otigon/automated-jb2a-animations) modules.

This module was originally created by Stenderpaval and is currently being maintained by Dafto.

## Use Cases

- The party is attacked by two dozen goblins and the GM doesn't want to resolve each attack individually
- You have a Circle of the Sheperd Druid or School of Necromancy Wizard and want to let them run 10+ summons without bogging down combat turns
- The big boss monster has 6 claw attacks and a tail attack and the GM wants to focus all the attacks on one poor character without having to roll each action separately, or keeps loosing count halfway between the rolls
- Your level 5+ character wants to use all their extra attacks on one monster but doesn't want to click through each one

## How to install

You can install this module by searching Foundry's package browser or by pasting this url in the corresponding text field of Foundry's package installer: `https://raw.githubusercontent.com/daft-develop/mob-attack-tool/main/module.json`. The module has no required dependencies and is only available for the D&D 5e system.

## How to use

After activating this module, a new button appears in the token controls bar.

![dice icon](images/dice-icon.png)

By default this button is only visible to users with the GM role, but this can be changed in settings. To begin using Mob Attack Tool, make sure you have at least one token selected and at least one token targeted before you click the button.

A dialog window will appear, populated with the weapon options of the selected tokens and a checkbox. Tick the checkbox of the weapon(s) you want to use for the mob attack. Mob Attack Tool can also automatically select weapons that are part of a multiattack ability, or just the weapon option that deals most damage. Once the dialog is open, changing your selection or targets will update the dialog automatically.

Clicking on the Mob Attack button in the dialog window will then whisper a message to the GM (by default) with the mob attack results, showing hits, misses, critical hits, and critical misses with attack modifiers included. Furthermore, the weapon item is rolled the number of times that an attack would hit and a damage total is calculated.

If the MidiQOL module is installed, enabled, and activated within Mob Attack Tool settings, the damage roll is handed off to MidiQOL, which may then apply the damage to targets for you (or however you've configured MidiQOL)

If the Dice So Nice! module is installed, enabled, and activated within Mob Attack Tool settings, on screen dice will be rolled for both attacks and damage. Optionally, attack dice can be hidden and only damage rolls shown.

If the Automated Animations module is installed, enabled, and activated within Mob Attack Tool settings, attack animations configured by Automated Animations will play for each successful hit.

Instead of rolling for each mob, a lookup table can be used instead which will determine a fixed number of attacks based on the number of creatures and attack bonus vs ac difference. This table can be manually adjusted in the settings menu.

## Limitations

- Currently damage is just rolled without saves or condition checks. Mobs of ghouls biting will not trigger any paralysing effects
- Older versions of this module worked with grouped initiative modules, but isn't actively supported in newer release. It might still work but hasn't been tested recently

## New

Make sure to read through the [latest release notes](https://github.com/daft-develop/mob-attack-tool/releases) to see what the newest features are.

## Examples

This is what the Mob Attack dialog looks like (as of v0.2.18) with multiattack autodetect + autoselect enabled. (Also shown are [JB2A Animated Assets](https://foundryvtt.com/packages/JB2A_DnD5e) triggered by a macro that makes use of Midi-QOL's On Use Macro field).

<img width="979" alt="MAT-v0 2 18-on-use-macro-JB2a" src="https://user-images.githubusercontent.com/17188192/122660094-a3da2880-d17e-11eb-8332-44f684868bff.png">

Below are some (older) GIFs that give a brief idea of how you can use Mob Attack Tool.

<details>
  <summary>Click to show GIF of Mob Attack Tool</summary>

  ![MAT-video-v0 0 3](https://user-images.githubusercontent.com/17188192/110196581-c81b2f00-7e45-11eb-908a-f0fd73567e10.gif)
</details>

<details>
  <summary>Click to show GIF of Mob Attack Tool + Midi-QOL</summary>

  ![MAT-video-midi-qol-v0 0 3](https://user-images.githubusercontent.com/17188192/110196624-0fa1bb00-7e46-11eb-9ec1-ade1ef8dff96.gif)
</details>

For more elaborate examples and screenshots, please head over to [EXAMPLES.md](EXAMPLES.md). (Note: the examples are currently quite outdated, but they should still give a general overview. Mob Attack Tool can do much nowadays than what is shown in the examples. Browse the [latest release notes](https://github.com/daft-develop/mob-attack-tool/releases) to find out what exactly.

## Planned improvements

* Further (optional) automation of the initial selection of tokens
* Some documentation and better structuring of the repo
* Multiple target selection enhancements
* Better incorporation of damage rolls to make use of latest 5e system enhancements

## Bugs / Feature Requests

Have an issue or think the module could use a new feature? Create a new [Github issue](https://github.com/daft-develop/mob-attack-tool/issues)!

## Translations

Mob Attack Tool currently supports these languages:

* English
* Korean (translation provided by KLO (discord : KLO#1490). Thanks, KLO!)

## Inspirations

* This module was inspired by [Multiattack 5e](https://github.com/jessev14/Multiattack-5e).
* The map shown in the examples was made by ~~Printable RPG~~ Spellarena. You can check out more of their beautiful maps on the [Spellarena Patreon](https://www.patreon.com/m/spellarena).

## Contributors

* Stenderpaval was the original author of this module and largely responsible for all the great features it provides
* Juanfrank has kindly given feedback and helped me out with condensing damage formulas.
* mike-marshall0164 has fixed various aspects of the individually rolled attacks.
* Many thanks to members of the League of Extraordinary Foundry VTT Developers for module development advice, including how to set-up GitHub Actions.
* 4cer improving the v10 fork with additional cleanup
