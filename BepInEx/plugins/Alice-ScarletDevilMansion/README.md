### Required by all clients

### Added presets for large 3+ lobbies and smaller 1-3 lobbies

### Doors are now destroyable by both enemies and players. Re-added AdvancedCompany compatibility code

### Trying out new lighting approach. If bad, please yell at me at my discord thread. Link found below

### 이제 비공식 한국어 패치를 넣고 실행할 때 걸리던 오류를 고쳐습니다

# The Scarlet Devil Mansion（紅魔館）

Adds the Scarlet Devil Mansion from Touhou as a possible dungeon for the snow moons (Dine, Rend, Tital). By default the chances are about 50% split between the regular mansion dungeon and the SDM dungeon. In the config, you can edit the spawn weight for any of the snow maps as well as any vanilla or custom moon.

We highly recommend [CullFactory](https://thunderstore.io/c/lethal-company/p/fumiko/CullFactory/) if your computer has framerate difficulties with this dungeon.

このページはまだ日本語に翻訳されていない（翻訳されるのだろうか？）。すまない

## Designed for All Parties

The dungeon features a config presets to accommodate the majority of party sizes and preferences.  These can be found in the _Presets section in the config. These will automatically overwrite the config settings as the preset values get updated. You can disable the automatic overwrite in the config as well. The preset feature is a lot easier to use with [Lethal Config](https://thunderstore.io/c/lethal-company/p/AinaVT/LethalConfig/).

You must load up Lethal Company once with this mod enabled to create the config. All configs are synced by the host.

![](https://i.imgur.com/H33RuzY.png)

The __Default__ preset. Designed for larger parties of 3 to 4+ players, this dungeon preset will create three main paths (as opposed to the game's single path) that's about half as big as a normal mansion. Scrap, enemy, and map hazard count are increased to fit the larger dungeon. 

![](https://i.imgur.com/7fQYIgV.png)

The __Small__ preset. Designed for smaller parties of 1 to 3 players, this dungeon preset is a smaller variant of the Default preset. It will instead create two main paths. As well, the scrap and map hazard count are only slightly increased.

![](https://i.imgur.com/XQDpxwL.png)

The __MoreLoot__ and __BitMoreLoot__ preset. Designed for parties who seek high risk, hish reward, these dungeon presets are variants of the Default and Small preset. These massively increases scrap, enemy, and map hazard count.

![](https://i.imgur.com/PFUOMbo.png)

The __Vanilla__ preset. Designed for parties who just want a vanilla dungeon experience. This tries to emulate Lethal Company's vanilla dungeon generation.

If tweaking is more of your style, you can still configure many of the dungeon's properties to your liking in the config. Just be sure to select the __Custom__ preset so they don't get overwritten. 

## Dungeon Layout

The map is a grayscale representation of what the Scarlet Devil Mansion could look like, with a mayor starting room, hallway corriders, and typical mansion rooms (bedrooms, libraries, kitchens, etc.). 

<details> 
  <summary>Click here to see the dungeon screenshots</summary>
  <img src="https://i.imgur.com/8bAX8Zb.png">
  <img src="https://i.imgur.com/wigscma.png">
  <img src="https://i.imgur.com/FRiiBmJ.png">
  <img src="https://i.imgur.com/pfTOFTK.png">
  
  <img src="https://i.imgur.com/VCpFZ1R.png">
  <img src="https://i.imgur.com/UmjWtc4.png">
  <img src="https://i.imgur.com/5M0itmD.png">
</details>

This dungeon uses modified dungeon generation code to create multiple main paths (as opposed to the base game's single path), then creates branching paths like normal. Furthermore, the dungeon will always be confined to a relatively small box. This is all done to increase the chance of the main paths connecting and forming a circular path. Please understand that this will increase dungeon generation times by a decent margin. None of this applies if you are using the Vanilla preset.

![](https://i.imgur.com/HXw3Fk3.png)

## Dungeon Features

Besides the dungeon's generation and tiles, the dungeon features a few unique mechanics that can shake up your scavenging adventure, or play a fun distraction.

<details> 
  <summary>Spoiler warning. Click here to see the features</summary>
  
  <br>
  <b>The Clock</b>
  <br>
  It's a clock. Accurately tells the time but has a knack of breaking.
  <img src="https://i.imgur.com/qe9ftUl.png">
  
  <br>
  <b>The Doors</b>
  <br>
  Doors, regular or locked, can destroyed by both players and enemies. Players require a shovel or shotgun while an enemy just has to be angry.
  <img src="https://i.imgur.com/JgrSIvA.png">
  
  <br>
  <b>The Portraits</b>
  <br>
  Rotateable portaits can be found on tables and dressers. They serve no other purpose.
  <img src="https://i.imgur.com/APWECSn.png">
  
  <br>
  <b>The Painting Event</b>
  <br>
  A high value scrap item. Snatching it will summon a dangerous enemy and even more scrap. A maximum of 2 can spawn.
  <img src="https://i.imgur.com/msj8prZ.png">
  
</details>

## Enemies and Vents

The dungeon uses summoning sigils to summon its enemies as opposed to vents. This is only a visual change. All enemies featured in this dungeon can only spawn inside the mansion.

![](https://i.imgur.com/FPW9D7o.png)

<details> 
  <summary>Spoiler warning. Click here to see the enemies</summary>
  <br>
  <b>The Knight</b>, a Coil-head variant
  <br>
  Acts like a regular coil-head, but is noticeably slower and prefers spawning from statue props, especially ones passed by scavengers.
  <img src="https://i.imgur.com/tV8Nw0A.png">
  
</details>

## Dungeon Items

The dungeon contains a few unique scrap items that can only spawn inside the mansion. They each contain a very unique interact feature.

<details> 
  <summary>Spoiler warning. Click here to see the items</summary>
  <br>
  <b>The Decorartion Crystals</b>
  <br>
  An average valued scrap item with a bit of weight. Comes it many colours. Can be combined with a flashlight in your inventory to create a new decorative flashlight with a recharged and improved battery, a colored light bulb, 50% of the crystals original value.
  
  <img src="https://i.imgur.com/bYaIofR.png">
  <img src="https://i.imgur.com/2OQdNlf.png">
</details>

## Roadmap in General

The development process is generally split into 3 distinct parts:

* Create more rooms, room variants, and polish up the current ones with props, lighting, etc.
* Add touhou-themed enemies and scrap items
* Add dungeon mechanics/features (for example the factory's appartatus and jumping puzzles)

There is a slim possibility that I add a custom moon, but that's so way down the line.

## Credits

Touhou owned by Team Shanghai Alice (ZUN)

LadyEbony.itch.io - Code, Dungeon Design\
MarkLi.itch.io - 3D Environment Assets (Rooms)\
Vinyis.itch.io - 3D Environment Assets (Hallways)\
@grandteki (Discord) - Various 3D Assets\
@Schmagons (Instagram) - 2D Art\
YeeHaw - Portait Art\
@Zaggy1024 (Discord) - For their sick help in getting Deep Profiling to work\
Nitori.itch.io - For their sick advice\
peacock-roy.itch.io - SFX

Released under Creative Commons Attribution License. If you'd like expand upon my work, while I would apprecite it you don't have to ask for my permission. You only have to include the text blob above, with the names and their contributions, somewhere reasonably visible in your mod page or whatever you doing.

If interested, the map assets were originally used in these two fan games. [Utusuru](https://nitori.itch.io/utsuru) and [Gensokyo Komarunner](https://nitori.itch.io/gensokyo-komarunner).

## Contact

Any complaints or questions can asked in this [discord thread](https://discordapp.com/channels/1168655651455639582/1195583267546595389). You can also dm personally at this [discord](https://discord.gg/M7aZKP9Qvc), LadyRaphtalia.

日本語がちょっとできるよ。コメントや質問やモンクがあったら、この[discordのスレッド](https://discordapp.com/channels/1168655651455639582/1195583267546595389)に書いてください。さらに、この[discord](https://discord.gg/M7aZKP9Qvc)でLadyRaphtaliaに直接メッセージを送ってください。

