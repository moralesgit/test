# Changelog

<li>2.0.15<ul>
<li>Now requires LLL 1.1.6 for stability.
<li>Dungeon no longer generates on start (fixes errors with new version of LLL)
<li>Due to LLL changes, no more haunted ItemDropper audio!
<li>Replaced the sandy audio with new audio created by one of our new team members, Oli! It's alot less harsh on the ears. You will be hearing more of their sound designs over time :>
<li>Fixed a bunch of small holes in terrain. Some still may be present.
<li>Fixed the main platforms mesh - it will no longer hide quicksand decals underneath it. It may on very rare spawns render slightly awkwardly (where its partially invisible, with a hard line) but this is unfortunately unavoidable due to how quicksand projectors are generated.
<li>Rainy weather temporarily disabled due to Quicksand no longer rendering on newer patches.
<li>Fixed a statue box collider not being correct.
<li>Fixed Dungeon Generation rates to match vanilla values. (Factory(39, Manor(300)))
<li>Story log has a new temp model and is ready for full implementation next LLL update.<ul>

<li>2.0.14<ul>
<li>This is a non-update. I have closed my channel in the LC Modding discord in order to open up a discord server specifically for future updates regarding Egypt and future projects! You can find the discord here:</ul> https://discord.gg/AqdawTWsTx

<li>2.0.13<ul>
<li>Fixed broken DunGen scripts, level now loads properly. Woops.</li></ul>

<li>2.0.12<ul>
<li>Fixed a box collider.
<li>Started implementation of DunGen assets under the hood (has no effect on current gameplay)</ul>

<li>2.0.11<ul>
<li>Drastically reduced vertice count of terrain mesh down to 14k. This should significantly help with performance.
<li>Removed one of the two fogs and applied the 3d noise texture to the primary fog, and made it denser to increase visibility at later times of day.
<li>Fixed a rock being out of place.
<li>Removed a significant amount of Mesh Colliders and replaced them with box colliders.
<li>Fixed a rock not rendering when it was supposed to be near the pyramid</ul>

<li>2.0.10<ul>
<li>Quicksand should render on Terrains now - Rainy weather type has been added to EGypt.
<li>Terrain material has been changed from Terrain2Mesh to HDRP/TerrainLayered, enabling the former comment. However, to a keen eye the terrain quality might look *slightly* worse, this is due to a half in quality for the Splatmap from 4K to 2K. 
<li>Adjusted the fancy pyramid tip.</ul>

<li>2.0.9<ul>
<li>Fixed a box collider to be a trigger collider.
<li>Fixed a soft-lock hole in the terrain.
<li>Made the pyramid tip fancy.
<li>The trello is now public.</ul>
<li>2.0.9.


<li>2.0.8<ul>
<li>Fixed water kill trigger.
<li>Re-adjusted some audio values.
<li>Fixed a few colliders.
<li>Removed ItemDropper holiday music.
<li>Adjusted scrolling sandstorm fog to be more dense.</ul>


<li>2.0.7<ul>
<li>Fixed a pillar collider.
<li>Fixed ambient audio being way too loud upon exiting the dungen.</ul>

<li>2.0.6<ul>
<li>Some small collider fixes.
<li>Repaired NavMeshLinks - you can't hide from dogs in certain places anymore.
<li>Fixed a collider on one of the entrances from double NavMesh rendering.
<li>Removed erreneous terrain from rendering in the sky (woops).
<li>Removed some colliders from the outside of the map to reduce load time.</ul>

<li>2.0.5<ul>
<li>Re-handled Terrain Mesh to 1 chunk to fix a mesh corruption error.
<li>Terrain-mesh now uses HQ version for collider. This will increase load times, unfortunately.
<li>Egypt now uses LLL through a Scene loader as opposed to a Prefab, just like how LethalCompany loads its moons. 
<li>Double-rendered moon bugs now fixed.
<li>The main entrance should no longer teleport you to the fire exit.
<li>Fog adjustments
<li>Max Outside Enemy Power Count reduced to 21. 
<li>Max Daytime Enemy Power Count reduced to 19.
<li>Max Enemy Power count increased to 15.
<li>Enabled Mimics to be able to spawn on EGypt.
<li>Added a StoryLog (not fully useable with LLL).
<li>All monster anmd scrap spawns adjusted, check the Wiki for exact weights.
<li>All entrance colliders re-built.
<li>MiniMap guide added to Wiki! There is a second fire exit, you know.
</ul>

<li>2.0.4<ul>
<li>NavMesh has finally been, truly, solved, we should NEVER have to deal with this again. Enjoy!
<li>NavMesh specifics:
<li>All Entrance Teleports have been removed from the Environment GameObject.
<li>Environment GameObject set to Prefab.
<li>Environment NavMeshSurfaceData baked to NavMesh-Environment under Prefab and saved to Prefab.
<li>Fixed a pillar bridge to have NavMesh support so mobs can cross it.
<li>Terrain re-baked and holes have been removed.
<li>AINodes moved closer to TerrainMesh.
<li>OnStayTrigger error has been fixed near ship.
</ul>

<li>2.0.3<ul>
<li>You will no longer fall through the map, I mis-used the Terrain2Mesh export.
<li>NavMesh has broken, for seemingly no reason. This is causing a flood in the console and reportedly causing some performance issues, we're investigating, but the moon is at least somewhat playable, and is currently the #1 priority.
<li>Terrain resolution fixed back down to around 200k vertices for mesh and collider, 4 chunks.
<li>LethalExpansionCore removed as dependency.</ul>

<li>2.0.2<ul>
<li>Woops.
</ul>

<li>2.0.1<ul>
<li>2.0.1 has been given the added dependency of LethalExpansionCore, which I should've added for 2.0.0 for a smoother transition away from LethalExpansion. This mod is not actually required and CAN be removed safely if none of your other mods require LethalExpansion. If any mods, such as moons or scrap mods, require LethalExapnsion, you MUST keep LethalExpansionCore installed for EGypt to work properly with LethalLevelLoader. LethalExpansionCore will not be kept as a dependency past 2.0.1
<li>Terrain Mesh & Collider vertice count reduced by 10%.
<li>Terrain material is now GPU instanced.
<li>Terrain chunk count reduced to 16 total chunks at lower resolution.
<li>Pillar colliders re-made from the ground up, no more getting stuck in them.
<li>Alot of the above changes should drastically reduce initial load time and improve performance on lower end hardware.
<li>Stripped scrap and enemy instances in-editor which should have HEAVILY reduced file size and load time.
<li>Fixed a little pixel "sun" in the sky that was weirdly parallaxing.
<li>Adjusted Spawn nodes to be slightly higher on Y axis to avoid clipping.
<li>Adjusted some spawn nodes to account for newer pyramid and terrain placement.
<li>Adjusted some spawn nodes to make the moon feel more lively at various times of day.
<li>Adjusted enemy power values to be closer to original Egypt values pre-LLL.
<li>File size reduced by ~70%</ul>



<li>2.0.0<ul> 
<li>LETHAL EXPANSION IS NO LONGER REQUIRED!
<li>The moon has been flipped 180 degrees, so the exterior (and thus your initial view) sees the pyramid, main entrance and two main pathways (yes there are two!)
<li>Exterior ambience audio has been fixed.
<li>Fire exit models have been added.
<li>Factory interior chance increased.
<li>Light pillars have been added to increase visibility during night time, and to guide players towards the main entrance.
<li>NavMesh is no longer baked by me, so no more navmesh hell!
<li>ItemDropper has been remade from the ground up, should work like vanilla!
<li>A second fire exit has been added closer to the main entrance.
<li>Terrain mesh has been changed, pyramid, main entrance has been moved closer to the ship. The pathway from the jumping puzzle to the pyramid has been shortened.
<li>Stormy weather is back!
<li>Scrap rates finalized at 300-700 min/max total value to match other moons, while total scrap remains fixed at 16 to 22.
<li>Interior size changed to 1.6 to match intended goals of higher level intermediate level.
<li>Moon price dropped from 200 to 60 credits. You can go here at the beginning of an expedition, but with no gear.
<li>Enemy spawn rates will now closely resemble march interior.
<li>Travel time to moon reduced from 4 to 2 seconds.
<li>Moon confirmation dialogue now reflects how many credits you have remaining.
<li>Internal moon string changed from desertmoon to egypt (for you dungeon-adding folk)
<li>Moon will no longer be ranked BB but will now appropriately be ranked B+.
<li>Planet now has a texture if you d- fail to comply with the quota on EGypt.
<li>All dungeon content types are currently being allowed due to the usage of LethalLevelLoader, but this will change when the DunGen is added next patch. Check out the discord for sneak peeks :>
<li>New Thunderstore icon</ul>

<li>1.0.8<ul>
<li>Adjusted scrap spawns to be more in-line with moon design. 
<li>Minimum scrap 14 >> 16, Maximum scrap 26 >> 22.
<li>Fixed terrain collider resolution.
<li>Fixed colliders on some meshes near the landing platform to be less complex.
<li>All rocks now have convexed colliders for performance optimization. This might make it appear as if you're floating on air in some spaces, but this is intentional behavior.
<li>Replaced NavMeshLinks for jumping puzzles with OffLinkMeshes so enemies outside will Jump as opposed to walking across open air.
<li>Slightly lightened the color of and reduced density of desert winds to help visibility at later time of day - this is now more in line with the rest of LC.
<li>Reduced spawn chance of Leviathans earlier in the day.
<li>Improved main platform texture.</ul>

<li>1.0.7<ul>
<li>NavMeshes are my worst nightmare. More fixes. This stuff breaks often, strong apologies.
<li>Replaced the mesh at the main platform as I believe this might have been causing many of the navmesh issues in the first place.
<li>Started development on custom DunGen aka Interior (this will take a long time)
<li>Adjusted spawns during daytime.
<li>Removed the item dropper tower because it was giving way too many navmesh issues.
<li>Fixed some objects changing LOS types incorrectly.
<li>There is now a wiki tab on the thunderstore website page that will list current known issues!
</ul>

<li>1.0.6<ul>
<li>MASSIVE NavMesh overhaul. Again. Stuff should stop spawning at 0,0, stuff should now obey the colliders of the platform. SHOULD. PLEASE.
<li>Worms can kill you now!
<li>More spawn fixes - things should spawn appropriately outside.
<li>More details outside, should feel less empty.
<li>Entrance scan be scanned from slightly further away.
<li>Changed terminal name from E Gypt to EGypt so it's more obvious that the route name does not have a space in it.
<li>Adjusted interior spawn power range to match March.
<li>Adjusted dungeon size to 1.3 from 1.
<li>Increased Dungeon Type 1 chance to 15% from 1%.
<li>Added Sandstorm Ambience sound outside.
<li>Adjusted jumping puzzle, again. Fixed "safe spot" within it, too.
<li>Changed planet description to match LC's moon style.
<li>Initial flooding value fixed to not be unplayable.</ul>

<li>1.0.5<ul>
<li>Major NavMesh fixes. (But still might not be perfect)
<li>Lots of re-tagging, things should sound the way they should.
<li>Many optimizations and other small fixes.</ul>

<li>1.0.4<ul>
<li>Fixed entrance colliders.
<li>Updated spawnrates for enemies across the board.
<li>Updated turret and mine rates.
<li>Fixed some path ways and nav meshing.
<li>Made the stone pathway a bit more challenging.
<li>Removed temporary mesh on fire exit entrance.
<li>Temporarily disabled Rainy and Stormy weather until SDK has a fix for weather removal bug.</ul>

<li>1.0.3<ul>
<li>Fixed Fatal Error.</ul>

<li>1.0.2<ul>
<li>More Collider Fixes</ul>

<li>1.0.1<ul>
<li>Fixed Pillar & Stair Colliders to Loot Instancer</ul>
