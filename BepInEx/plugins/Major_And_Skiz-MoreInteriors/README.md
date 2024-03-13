## More Interiors [2.5.0] - Major_And_Skiz
 Tired of always going to the facility or the manor? This mod adds some new interior tile sets for your crew to scavenge in! Only the bunker tileset is finished as of now, but we're already working on more.

 The Bunker - A dark maze of underground tunnels that's both cramped and expansive at the same time. If you didn't like thumpers before, wait till you're trapped in a long tunnel with one. 


## Features:
- A WWI Military Bunker tileset to add some variety to your everyday scrap runs.
- Dynamic fire exits, scrap spawning, and enemy spawning.
- This plugin should work with custom moons!
- Apparatus spawns in bunker tile
- Army Style Scrap
- Custom Scrap Added OldRadio,Canteen,Armyhelmet,RockingHorse,Gramophone,WheelRim,WireSpool,TypeWriter
- Rat Creatures that roam around inside


## Planned Features:
- Additional Tilesets
- Custom Scrap pools for each interior tileset
- Armory Tile
- Interactable Bunker Objects
- Lore Documents

## Configure Settings:
By default, the bunker has chance to appear on Offense and March - if you want to change the appearance rate, or change what moons it can appear on, the config settings allow for the following settings:
- Change abilty to add in moon rarity values (EXAMPLE: Vow:200,Titan:400)
- Set the bunker to always appear
- Set length of the bunker appearing
- Set Rarity of Outpost 31 to appear default 9999

## Config
### BunkerRarity: 
- How likely for Bunker to appear on moons (0-300) 
### BunkerMoons: Set to Following presets 
- "List" : Individual moons only with rarity weights 
(EXAMPLE: Exerimentation:20,Titan:9999)
### BunkerDungeonMoonsList: 
#### Note BunkerMoons must be set to list! 
- Can be used to specify a list of moons with individual rarities for moons to spawn on.
(EXAMPLE: Offense:100,March:500,Titan:9999)
### BunkerGuaranteed: 
- if Enabled (True) Sets all Presets to 9999 will overide custom any Set to BunkerMoons and BunkerMoonsList if Defined - -
- (EXAMPLE BunkerMoons- "All" sets all moons to 9999) 
- (EXAMPLE BunkerMoons - "List" BunkerMoonsList - vow10,Experimentation100) will set Vow and Experimentation to 9999

## How to Install:
- Make sure you have [BepInEx](https://thunderstore.io/c/lethal-company/p/BepInEx/BepInExPack/) & [LethalLib](https://thunderstore.io/c/lethal-company/p/Evaisa/LethalLib/) & [LethalLevelLoader](https://thunderstore.io/c/lethal-company/p/IAmBatby/LethalLevelLoader/) & https://thunderstore.io/c/lethal-company/p/Evaisa/HookGenPatcher/ 
installed.
- Download and unzip the mod.
- Merge the BepInEx folder from this zip with the one found at: (`\GAME_LOCATION\Lethal Company\BepInEx`)
- Optional: Launch and close the game to generate config file.

# Credits
#### Majorblue7 - Project Lead, Programmer, Level Designer, Tester,
#### Skiz - Project Lead, Level Designer, Art Direction, Q+A

### A huge shoutout to these people and their mods for help and reference!

#### Evaisa- Lethallib

#### IAmBatby- LethalLevelLoader

#### Badhamknibbs- SCP Modding Scripts for DunGen Example and Config setup - SCP Foundation Dungeon
 https://thunderstore.io/c/lethal-company/p/Badham_Mods/SCPFoundationDungeon/

#### Scoopy - Code and Scripts Help - Scoopys Variety Mod
 https://thunderstore.io/c/lethal-company/p/scoopy/Scoopys_Variety_Mod/

Go Check out there Mods 

**NOTE:** This mod requires everyone in the lobby to have it installed to avoid desync; everyone must also share the config settings (config sync may be implemented later)


Have fun exploring!
