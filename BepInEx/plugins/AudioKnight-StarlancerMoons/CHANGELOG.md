- 1.3.0
  - **Changes are for each moon unless otherwise specified.**
  - Another chonky performance update.
  - Swapped out the volumetric clouds for cloud layers. They're more performant and I think they actually look better.
  - Adjusted fog thickness.
  - Changed the global volumes that contained general fog settings to local volumes in order to prevent fog settings from affecting interiors.
  - Added fog exclusion zones around key areas
  - Solace
    - Added 2 fire exits. Increased dungeon size multiplier from 1.25x to 1.35x to account for the increased number of entrances.
    - Replaced some trees to prevent them from clipping through the ship.
    - Smoothed out some terrain near the ship that was potentially causing players to clip through the map.
    - Fixed missing tree colliders.

- 1.2.0
  - Big performance update.
	  - Cleaned up some trees on Solace.
	  - Reworked LODs for trees on Auralis and Solace.
	    - As an added bonus, the file size is now smaller!
	  - Replaced combined meshes with their original variants and rebaked occlusion on all 3 moons.

- 1.1.1
  - Re-enabled "receive fog" on Solace's water material.

- 1.1.0
  - Improved performance on Auralis, Triskelion, and Solace.
    - Globally tweaked shadows, fog, and cloud effects.
    - Baked occlusion areas and a culling occlusion portal onto each moon.
    - Lowered Solace dungeon size from 1.8x to 1.25x (Slightly lowered total scrap amount to balance out the change, feedback is welcome as always.)
    - Removed some unnecessary objects from Solace that the player wouldn't see under normal circumstances.
    - Lowered Auralis dungeon size from 2x to 1.8x for performance.
	- Adjusted Triskelion's lighting and LOD groups.
  - Increased the trigger size of the hillside fire exit on Auralis to improve interactibility.
  - Slightly increased the exterior fogginess on Auralis and Triskelion.
  - Applied a temporary adjustment to the global fog volumes to make them not ruin the interiors. I'll be working on a better solution.
  - Fixed an incorrect tag on the main building platform on Auralis.
  - Fixed foliage coloration on Solace.
  - Fixed the water triggers on Solace being too small.

- 1.0.1
  - Updated the description. (So much double and triple-checking, yet it still slipped past me ; - ; )

- 1.0.0
  - Working with a new editor set-up, thanks **Nomnom**!
  - Switched to a new lighting workflow, based on **sf Desat's** resource pack. Thanks!
  - Updated dependencies. Now depends on Starlancer AI Fix.
  - Released new moon, 74-Solace.
  - Auralis changes:
    - Added ambient sounds, both generalized (like outside wind) and randomly occurring.
    - Fixed the navmesh to the ship. Previously it was missing the Off Mesh Links for the ladders so certain enemies were unable to use them, making it far too safe.
	- Adjusted the navmesh around the small building to prevent Forest Keepers from trying to mate with it.
	- The water on Auralis is cold enough to cause immediate hypothermia, and has been update to reflect as such. (Touching the water now causes you to take damage. Don't fall in.)
	- Increased the number of Outside AI Nodes.
	- Increased turret and landmine spawns.
	- Added a certain interior enemy to the outside spawnlist. Flowers now grow amongst the trees.
	- Continued optimizing performance.
  - Triskelion changes:
    - Added ambient sounds, both generalized (like outside wind) and randomly occurring.
    - Fixed the navmesh to the ship. See above.
	- Increased the LOD distance slightly to reduce texture pop-in.
	- Increased the number of Outside AI Nodes.
	- Increased turret and landmine spawns.
	- Added an ***extremely*** rare chance for a certain interior enemy to spawn outside. Eyes up, Starlancer.
	- Continued optimizing performance.

- 0.5.7
  - Updated dependencies.

- 0.5.6
  - Reactivated Triskelion, fixing the "Random Seed: #" soft-lock and broken spawns.
    - Here's my understanding as to why it broke, which may be incorrect, but the result is the same anyway:
	  - I use blank references to vanilla files to make my files smaller. LLL searches for references in the mod's asset bundle and once they're loaded, they are destroyed. Auralis was first (because of the alphabet, I guess?) which is why it never broke, so when LLL went to load Triskelion's data, it had already nulled out the references.
	  - The reason the "Random Seed: #" lock-up happened is because the spawning of map objects (like turrets and landmines) takes place alongside dungeon generation. When the references were "null" this caused the generation to stall.
	  - The reason the spawns had broken was the same, it just didn't lock-up the game because spawns happen after dungeon generation, and null references there are treated as 0s instead from what I can tell.
	  - My fix was to duplicate my blank references into a different folder, thereby creating seperate assets for LLL to load (and subsequently delete), thus resulting in things working again!
	    - ~~my agony today was endless, the darkness infinite, please send supplies I'm behind enemy lines the baboon hawks are closing in on m----------~~
  - Attempted to fix the issue on Triskelion where falling off of the exterior platforms into the green depths below would result in the player's body ending up in the dungeon somehow.
  
- 0.5.5
  - Added LCMaxSoundsFix by Hardy as a soft dependency. It's not actually required to run Starlancer, but it resolves the issue with audio cutting out when too many audio sources are present, both on modded moons and I presume in vanilla, so in order to get the best experience I'll tie it in as an optional.
  - Added navmesh on Auralis and Triskelion to allow the Masked Employees and Outside Entities to climb into the ship. Live in fear, for the company's ship may be your tomb.
  - Locked away Triskelion for the time being. It will no longer show up in the terminal, attempting to route to it from the Moons list will inform you that it is unavailable, and routing to it from elsewhere is prohibitively expensive (999999c). If you really want to go explore it for fun, by all means mod your credits up, but I will be disregarding Triskelion bug reports for now.
    - It no longer gets stuck on "Random Seed: #" but the spawns are completely broken.
    - Widened the staircases and rebaked the navmesh on Triskelion to help with the Baboon Hawks getting stuck.
    - Removed one possible outside spawn point to declutter.
  - If you so desire, you may revert to LLL 1.0.7 and StarlancerMoons 0.5.3 to reactivate Triskelion in a stable setup.
  
- 0.5.4
  - Updated to LLL 1.1.4
    - This update will automatically generate a section within the LLL config file to customize the following:
	  - Planet Route Price
	  - Day Speed Multiplier
	  - Whether or not the planet has time at all
	  - Hiding and registering the level in the terminal
	  - Min/Max Scrap Item Spawns and Value
	  - Scrap Spawning List
	  - Max Inside, OutsideNight and OutsideDay Enemy Power Count
	  - Inside, OutsideNight and OutsideDay Enemy Spawning List

- 0.5.3
  - Fixed a visual issue with the liquid/gas below Triskelion sometimes having its original color bleed through.
  - Moved the surprise tool so that it's not in such a cheese-able spot. It still respawns each time (no way to change this just yet) but I want to keep it in the level regardless.
  - Fixed the fire exit doors on Auralis not having the correct material.
  - Removed the possibility of Stormy weather on Triskelion. A shovel planet should not have anti-shovel weather.
  - Adjusted spawn rates again. I went a little heavy-handed in 0.5.2, but I don't have the old spawn curves, so I used some vanilla curves for reference this time.
  - Rebaked navmesh on Triskelion to hopefully help Baboon Hawks not block up the stairs as much.
  - Removed some disabled audio sources on Auralis. Unity's audio limitation is frustrating, but I'm hoping the next LLL update will help with this.

- 0.5.2
  - Adjusted spawn rarities and power caps on both Auralis and Triskelion. I had been misunderstanding the way the spawning works, so it should be more consistent (and slightly less brutal on the exterior of Auralis early in the day).
  - Made one of the fire exits on Triskelion unreachable without an extension ladder or jetpack, for balance purposes. It is still possible to hop down from that area onto the platform below without suffering fall damage.
  - Decreased the number of exterior spawn points on Triskelion.
  - Slightly increased the chance for the mansion tileset to spawn on Triskelion.
  - Made some small adjustments to scrap spawns on Triskelion.
  - The immense pressure of the gas below the Triskelion outpost is now immediately lethal.
    - No more waiting until you hit the "out of bounds" plane :)
  - Added a surprise tool that will help you later.

- 0.5.1
  - Adjusted fog and lighting on Triskelion for performance reasons.
    - Removed spot light objects from the wall lights. This hurt a bit for me, but performance is more important.
    - Shortened the distance to where fog blocks out light. (I think this makes it so it doesn't have to calculate stuff as much? Seemed to help performance regardless.)
  - Found more textures to downsize.
    - This change seems to have boosted Auralis' performance as well.
  - The changes here have given StarlancerMoons near-vanilla performance for me, but as always please report any issues.
  - Adjusted spawn rates on Triskelion to be a little less brutal.
  - Slightly increased total scrap value for Triskelion.

- 0.5.0
  - Skipped 0.4.0 to match Moons with the Modpack version.
  - Released new moon, 27-Triskelion.
  - Increased Auralis' base fog amount. Still haven't found the solution to making the foggy weather cover more of the map but as soon as I do I'll have it fixed.
  - Removed the exterior fan noises. Too many audio sources at once can cause sound to cut out apparently, which is a base Unity issue.
  - Fixed the problem with the snow texture on the ground not rendering properly. This was due to some issue in the alpha channel of the texture.
    - Decreased the intensity of the lights now that the ground is actually white.
	- This may have an additional benefit that I didn't foresee:
  - Snow footprints are now working! Footstep sound changed back to Snow from Grass. There shouldn't be as much of an issue with the audio cutting out now that I've removed the fan noises.
  - Found a slew of textures that I forgot to downsize, StarlancerMoons is now much smaller in size.
  - Removed the snow particle system. Too much of a drain on performance for what little it added.
  - Hopefully fixed the small building not defending you against Forest Keepers.
  - Heard reports that the forests were too safe on Auralis, this is no longer the case. The forests no longer harbor the indigent.
  - Fixed the sun not actually being animated. How did no one report this.
    - As a result, Auralis actually gets dark now.
  - Fixed a clipping issue on one of the shipping containers.

- 0.3.1
  - Adjusted the AudioReverbTriggers on the map.
    - Changed the outside reverb preset from "Alley" to "OutsideSnow"
	- Added "SmallRoomReverb" to the small building.
  - Lighting adjustments.
    - Disabled bloom, as I didn't realize how fuzzy it was making everything.
  - Added an occlusion area to the general playable area. Might help with performance?
  - Changed footstep sounds around the map.
    - I've reverted the terrain back to using "grass" footsteps due to an audio bug I experience solely when I use the snow tag. (And because I feel the snow crunch is unnecessarily loud.)
	- The stairs now use metal footsteps.
  - The fans attached to the facility now play a quiet, looping audioclip.
  - Added level tags "Snow" and "Ice"
  - Adjusted navmesh values to be closer to some of the vanilla moons.
  
- 0.3.0
  - ***THE LLL UPDATE***
  - Converted StarlancerMoons to use LethalLevelLoader. As a result, LethalExpansion (or LethalExpansionCore) are no longer required, and this mod is now dependent on LethalLevelLoader.
  - Updated the description of Auralis.
  - Adjusted enemy spawn weights.
  - Adjusted scrap spawn weights.
  - Tweaked enemy spawn chance throughout the day. Should be slightly more calm at the beginning of the day now.
  - Changed the tag for the terrain and ice floes to "Snow" to allow for snow footstep sounds. This caused some audio issues when built with LE, so please let me know if these issues return.
    - Hopefully I can get snow footprints working too, but I haven't figured it out just yet.
  - Updated water system for the ice lake.
  - Tweaked the snow particle system.
  - Altered the material on the ice floes so they'll stop having a weird error shader bleeding through from their core.
  - Fog and lighting adjustments.

- 0.2.2
  - Fixed the issue where rain wouldn't resume upon leaving the facility during rainy or stormy weather.
  - Updated snow particle system.
  - Updated moon description.
  - Decreased spawn weighting for Jester, DressGirl, and SporeLizard.

- 0.2.1
  - Added some extra colliders to the small building to stop Forest Keepers from never losing sight of you.

- 0.2.0
  - Auralis is now part of "Starlancer Moons" and bundled into the "Starlancer" modpack. I'll be releasing some custom music in a couple of days as a separate mod. This way everyone has the choice of what Starlancer content they'd like to use.
  - Starlancer Moons is now dependent on "Lethal Expansion Core" instead of "Lethal Expansion", since LE's author is looking to step down from modding for the time being.
  - Completely reworked the terrain down to the intended playable area. This should improve performance, but please let me know.
  - Removed a bunch of pointless baked lighting data that was bloating the file size. Oops. (The .lem file is now 57mb instead of 196mb)
  - Added a second fire exit.
  - Lowered masked enemy spawns slightly.
  - Decreased the size of the dungeon generation to be equivalent to March. My tests showed there was way too much empty space inside, even with the higher scrap amount that should be present.
  - Decreased the rate of outside enemy spawns slightly and decreased the cap to help limit the number of dogs. Baboon Hawks can now spawn.
  - Significantly increased the falloff of daytime enemy spawn rates. Removed Circuit Bees for thematic reasons.
  - Added a small exterior building halfway between the ship and the facility. ~~You are being watched~~
  - Added some environmental decorations.
  - Adjusted volumetric fog and lighting.
  - Hopefully fixed the issue where water isn't drowning employees >:|
  - Changed the tag on the ice floes to hopefully resolve some reported audio issues. If these persist, it's possible that it's a bug in the SDK. I'll keep a watch on it.
  - Decreased the routing cost to 750.
  - Lowered the chance for the mansion tileset to spawn.
  - Added collision to the walls around the doors. No idea how this didn't get discovered by anyone.

- 0.1.4
  - Adjusted scrap spawn rates on Auralis and removed certain low-value scrap (don't worry, duckies _can_ still spawn, just very rarely). It should be much more profitable now on average.
  - Performance optimizations.
  - Small adjustment to interior enemy spawn rates.
  - Very small adjustment to dungeon size.

- 0.1.3
  - Performance optimizations.
  - Fixed an issue where walking into the lake wouldn't trigger water effects.
  - The path to the fire exit is now shorter.
  - Fog adjustment.
  - Added footstep sounds.
  - Changed the color of the sun.
  - Changed orbit prefab for Auralis to Moon3.

- 0.1.2
  - Fixed item dropship not appearing. (Note for other modders: This was caused by a change to the dropship object in Lethal Expansion.)
  - Raised starting height of falling snow.

- 0.1.1
  - Fixed navmesh issues.
  - Fixed scrap falling through landing pad.
  - Shifted a tree out of the way of the ship's landing sequence.
  - Adjusted the ice floe path. It's still treacherous, especially while encumbered, but it should be a bit easier to make the jumps.

- 0.1.0  
  - Initial Release.
  - Added custom moon "Auralis".