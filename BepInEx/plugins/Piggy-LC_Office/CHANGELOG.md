## 0.0.3  

- Remove test item spawn.

## 0.0.4 

- moved to LethalLevelLoader.
- Changed the layout of the server racks.
- Fixed an issue where some items would not set the elevator as their parent object.
- Fixed some errors that occurred during interior generation.
- Lots of optimization work.
- Sadly no monster spawns yet :/

## 0.0.5 

- edited README.md

## 0.0.6 

- Changed the layout of the some room.

## 0.0.7 

- Fixed issue with guaranteed spawns on any moons.
- Changed the layout of the some room.
- Every song filters have been edited to make them less painful to the ears.
- Removed the cootie theme.
- Fixed the pitch of the shop theme the same as the original.

## 0.0.8 

- Fixed an issue with guaranteed spawns on every moons. now appears randomly on paid moons.
- Added configuration for interior spawns.
- Temporarily completed the unfinished start room.
- Created a staircase on the left side of the start room (ladder included, so two handed items cannot be moved).
- Fixed extreme frame drops in game before landing or when on a moon with no office interiors spawned.
- Revamped trap rooms (still unfinished, you won't see any changes in actual gameplay).
- Added [OdinSerializer](https://thunderstore.io/c/lethal-company/p/Lordfirespeed/OdinSerializer/) as a dependency in preparation for LethalNetworkAPI v2.0.0.

## 0.0.9 

- Fixed some issues.

## 0.1.0

- Enemies can now spawn!
- Added a new enemy "Shrimp".
- Fixed an issue where navmesh agents could not navigate through staircase rooms (even though no enemies spawned)
- Compatible with LethalNetworkAPI 2.1.0.
	
## 0.1.1

- Added pictures to README.md.
- Fixed extreme frame drops occurring when an interior other than an office was created.
- Reduced the time it takes for an enraged Shrimp to reach its maximum speed(acceleration remains the same).
- Added configuration related to the spawning of Shrimp.

## 0.1.2

- Added “Satisfaction” value to Shrimp. Shrimp will now stop following the player for a while if they have enough food. (not tested)
- Fixed softlock occurring when shrimp spawn on all clients except the host.
		
## 0.1.3

- Added two large rooms.
- Added a prop to several rooms.
- Remodeled the starting room.
- Improved dungeon generation.
- Added Lung apparatus socket machine spawn.
- improved the elevator system, but haven't tested it yet.
- Fixed a bug where Shrimp's "Satisfaction" system did not work properly.

## 0.1.4

- s m o l Update
- Minor performance improvements for items.
- Fixed some bugs in the shrimp.

## 0.1.5

- Fixed a bug where elevator safety doors would not open when starting the game.
- Fixed a bug that caused RoundMapSystem to consistently error out on loading.
- The emergency exit is a bug we can't fix at the moment due to an error in LLL (or a DungeonFlow error in Office), and I'm talking to the LLL developers - sorry!

## 0.1.6

- Fixed some bugs.

## 0.1.7

- Added a new facility style stair room to replace the old stair room.
- Added a small LED next to the elevator panel to make it easier to see if the elevator is up.
- Remove some rooms (two door rooms and rooms with stairs) because the original file was broken... sad
- Removed test room.

- Made some improvements to dungeon creation.
- Reduced the overall size of assets.
- (Probably) fixed the sliding glass door. Once again.
- Fixed a bug where spray paint/blood was not visible.
- Changed the name from ShrimpSpawnableMoons to ShrimpSpawnWeight, so you need to reconfigure it. 
- Changed the text on the elevator panel.
- Fixed an issue where shrimp would not spawn properly in office interiors.

## 0.1.8

- Shrimp now spawns on a modded moon.
- Added configuration for Shrimp to set spawn weight on modded moon.

## 0.1.9

- Fixed a bug where staircase rooms had incorrect colliders.

## 0.2.0

- This update uses a lot of network variables and may cause some frame drops. Please let me know if you are experiencing severe frame drops.

- Synced Shrimp's hunger value.
- Separated the stairs and hallway in the Staircase room.

- Fixed a bug where:
- Shrimp could not open doors.
- Shrimp would occasionally look in strange directions.
- Shrimp's position and orientation were out of sync.
- Shrimp would not react when hit.

- Fixed a bug where you could get stuck in the walls of the staircase room.
- Fixed a bug where some rooms would spawn incorrect doors/no doors.

## 0.2.1

- Fixed bug where rooms would spawn overlapping.
- Fixed a bug where players who used the elevator even once would not respawn on takeoff.
- Fixed bug causing doors to be misplaced.
- Added exception handling for shrimp not syncing bug. Please let me know if you encounter this bug.

## 0.2.2

- Fixed bug where turrets would penetrate some walls.

## 0.2.3

- Added auxiliary power units to elevators(Compatible with FacilityMeltdown mod).
- If a apparatus within the interior was unplugged, the elevator was changed to be inoperable without the use of auxiliary power
	
- Shrimp desync issue is probably.. fixed.. again.. idk
- Fixed a bug where doors in some rooms were not positioned correctly.

## 0.2.4

- Added a ladder in case the elevator is unavailable for some reason.

- Fixed a bug where the doors would not open when the elevator automatically descended after taking Apparatus.
- Fixed a bug where rooms would spawn overlapping due to forgetting to set the bounds override

## 0.2.5

- Added little animation when placing Apparatus in an elevator.

- Fixed several bugs that occurred when lobby restarted.
- Fixed a bug where the doors would not open when the elevator automatically descended after taking Apparatus. again.

## 0.2.6

- Made some minor improvements to the elevator doors.

## 0.2.7

- Fixed a bug that occurred when taking Apparatus from interiors other than Office.

## 0.2.8

- Fixed a bug that occurred when taking Apparatus from interiors other than Office... Again.

## 1.0.0

- Out of beta.
- Fixed a bug where enemies could not enter staircase rooms.

## 1.0.1

- Fixed a bug where elevator doors would not open after taking Apparatus.

## 1.0.2

- Changed network variables to be initialized every time the moon is landed.

## 1.0.3

- Fixed an issue with overlapping start rooms.

- Shrimp has been nerfed:
- Shrimps will no longer chase players when they determine that they cannot chase them.
- Increased overall hunger reduction when eating item.

## 1.0.4

- Added 3 tiles(rooms).
- Added 5 scrap (Coin, Laptop, Screw driver, Toolbox, Wrench).
- Fixed scrap spawning.
- Fixed an issue where maps were generated too large.
- Elevator Apparatus system has been temporarily removed (for my sanity).
- Changed the door model.
- Reanimated the lung place animation(although it doesn't work).
- start room has been reworked and the elevator floors have been increased from 2 to 3(It may be reworked again in the future).

- Revamped the entire elevator system.
- Improved map generation and added override dungeon scaling config.
- Fixed an issue with vents being misplaced in server rooms.
- Added a config to adjust the volume of elevator music.
- Fixed a bug where shrimp could not recognize players.

## 1.0.5

- Changed the Dungeon Register.
- Removed BigDoorSpawn due to a bug.

## 1.0.6

- Fixed a bug where items would sometimes not interact with elevators.

## 1.0.7

- Fixed a bug that caused infinite dungeon generation.

## 1.0.8

- Changed the Dungeon Register again.
- Changed the Item Register.
- Fixed an issue with screwdrivers being assigned to mesh variants on laptops.
- Fixed incorrect item ID.
- Removed mesh variant from screwdriver.
- Assigned a main renderer for all scraps.

## 1.0.9

- Fixed a bug where more than 2 shrimp would spawn.
- Improved the item parent system.

## 1.0.10

- Changed the default for scrap spawn configuration to disabled. I will change it later when it is completely fixed.

## 1.0.11

- Reverted some changes to 1.0.4.

## 1.0.12

- Improved the AI of Shrimp:
- Shrimp will now move out of the way when it's in your way!
- Shrimp with no targets now have lower necks.
- The shrimp can now hear the sound and will look in the direction of the sound.

- Fixed an issue where the door in the start room was assigned the wrong texture.

## 1.0.13

- Fixed a bug that caused some rooms to overlap.
- Fixed an issue where the door in the start room was assigned the wrong texture.
- Changed the color of the elevator's apparatus to avoid confusion with the apparatus item.

## 1.0.14

- Removed LocalPropSet for intersections and created new ones for each room.
- Added simple feature to check if there is a path on each floor.

## 1.0.15

- Fixed a bug where walls in some rooms were generated strangely.... sry

## 1.0.16

- Added a wait time to the Shrimp's reaction when it takes damage.

## 1.0.17

- Changed elevator panel to allow you to move by floor from up/down.
- Fixed a bug where the start room path panel was displayed incorrectly.

## 1.0.18

- Increased spawn weight in start room.
- Removed render for elevator collider.

## 1.0.19

- Increased the weight of relatively short corridors and decreased the weight of long corridors.
- Increased spawn weight in start room again.

## 1.0.20

- Improved the AI of Shrimp.

## 1.0.21

- Fixed a bug where doors and blockers were spawned overlapping in a room.
- Fixed (probably) compatibility issue with CullFactory.

## 1.0.22

- minor fixes.

## 1.0.23

- Fixed some important bugs in Shrimp.

## 1.0.24

- Improved moons registration.

## 1.0.25

- now that the shrimp is satisfied, he won't look at the source of the noise.
- Shrimp's body now rotates as he looks at the source of the noise.

## 1.1.0

- Added a new enemy "Halt" (from DOORS).
- Added one room.

- Fixed some bugs.

## 1.1.1

- Made Halt's body darker.
- Stamina is no longer consumed during encounters with Halt.
- Removed vent in start room.

## 1.1.2

- Added a config to turn off custom camera shake for players with motion sickness.
- Lowered Halt's spawn rate.
- Increased "TURN AROUND" text size.
- Fixed an issue with reverb being applied to Halt's sound effects.
- Reanimated camera shake to be more intense.

## 1.1.3

- Increased brightness during Halt encounters (I had the game's gamma set to max lmao)

## 1.1.4

- Fixed an issue where Halt's eyes would not appear on screen when attacked.
- Increased the bounds of the start room.

## 1.1.5

- Added config to determine whether to increase the brightness when encountering Halt, For compatibility with Diversity's Full Darkness config. This config requires Diversity to be installed to work.
- minor fixes.

## 1.1.6

- Fixed a bug where terminal could not be quited.

## 1.1.7

- Changed Halt's config to a spawn "probability" configuration.

## 1.1.8

- Fixed an issue where Halt spawn probabilities were reversed.

## 1.1.9

- Changed the code that drops all items during Halt encounters to network function.

## 1.1.10

- Removed fire exit spawn in Halt's Hall.
- minor fixes.

## 1.1.11

- Reupload due to Thunderstore error.

## 1.1.12

- Now Shrimp is happier when he's full :D.