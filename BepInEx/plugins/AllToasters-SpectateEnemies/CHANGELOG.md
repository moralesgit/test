# Changelog

## v2.3.1
- Fixed an issue where certain custom enemy names would cause the config to fail to load

## v2.3
- Greatly improved the zoom feature (big thanks to [HalfyRed](https://github.com/Xenation/SpectateEnemiesFix/)!)
- Switched the configuration system back to BepInEx's
   - This should also add support for LethalConfig!
- Added a config option to disable the controls tooltip on the right side

## v2.2.1 (Hotfix)
- Fixed a crash caused by the only enemy alive being killed

## v2.2
(Big thanks to @1A3 for helping with this update!)
- Updated to support v47
- Added support for modded enemies!
   - Note for developers, your enemy MUST have an `EnemyType` for it to be picked up by SpectateEnemies
- Added zooming while spectating enemies, allows zooming from 1x to 10x zoom
   - Uses the scroll wheel by default, can be changed in the keybind settings
   - The current zoom level is displayed next to the `(Spectating: ...)` text
- Enlarged the config menu box a little to allow more room for modded enemy entries
- Shortened the controls text on the sidebar to be neater/less cluttered
- The mod will no longer attempt to spectate dead enemies
- The mod will no longer collect enemies disabled in the config as spectate targets
   - This should fix the issue where the first enemy spectated was sometimes a disabled enemy
- The list of spectate targets will now refresh when moving to the next enemy
- Improved some internal checks that were throwing errors in the console

## v2.1.1 (Hotfix)
- ACTUALLY fixed the issue where masked enemies could not be spectated

## v2.1
- Added 3 keybinds to the in-game keybind menu for most SpectateEnemies controls
   - [InputUtils](https://thunderstore.io/c/lethal-company/p/Rune580/LethalCompany_InputUtils/) is now required by the mod, so ensure you install it as well
- Fixed an issue where masked enemies could not be spectated (again)
- Fixed an issue where the mod would attempt to spectate players who are not connected

## v2.0
- Added a developer API to allow mod developers to access some SpectateEnemies information
- Added an in-game config menu to toggle spectating all enemies individually
   - The menu can be accessed with the "Insert" key
   - The menu is most likely temporary and will be moved to the in-game settings menu in the future

## v1.5
- Added the ability to spectate masked players
- Added a message that is displayed when there are no enemies available to spectate
- When spectating enemies for the first time in a round, the mod will now spectate the closest enemy to the player you are currently spectating
- Fixed another issue that would allow you to continue spectating enemies after the game ended

## v1.4
- Updated to support v45
- Fixed mod keybinds not working in the latest version
- Fixed keybind text not displaying in the latest version
- Fixed an issue that would cause the flashlight to remain on after the game ended
- Fixed an issue that would allow you to continue spectating enemies after the game ended
- Fixed an issue that would prevent the flashlight from being toggled after a vote to leave has been initiated

## v1.3
- "Added" a toggleable flashlight to the spectator camera (one already exists...it just wasn't enabled)
   - The flashlight can be toggled by clicking RMB
- Added code to attempt to fix some enemies showing up as "Enemy" when spectated
- Fixed an issue where the mod would sometimes fail to start spectating enemies
- The controls tooltips will now dynamically update depending on which side the player is spectating

## v1.2
- Increased camera zoom for all enemies
- Increased camera zoom even further for taller enemies
- Added a "Spectate Passives" config option to enable/disable spectating passive enemies
- Spectating now uses a toggle to swap between spectating players and enemies. The swap key is your "interact" key. (Default: E)
- Added a control tooltip in the top right to show the key for the spectate toggle
- The mod will now remember your last spectated enemy, if it is still alive

## v1.1
- Fixed an issue where mod values would not update upon the ship leaving or leaving the game
- Fixed the Spectating text so that it displays the actual enemy name and not their GameObject name

## v1.0
- Initial release