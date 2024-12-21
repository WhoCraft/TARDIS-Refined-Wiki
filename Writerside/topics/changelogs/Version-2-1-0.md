# Version 2.1.0 (UPCOMING)

![TARDIS Refined](tardis_refined_v2_1.png)

#### Bug Fixes
- Bug fix: Added "Compatibility" with [Diagonal Windows](https://www.curseforge.com/minecraft/mc-mods/diagonal-windows)
- Bug fix: Exception Ticking World [#388](https://github.com/WhoCraft/TardisRefined/issues/388)
- Bug fix: Nuka Console Duplicate Control Entity Failing Flight Dance Events [#376](https://github.com/WhoCraft/TardisRefined/issues/376)
- Bug fix: land pad dont work and crash on server [#377](https://github.com/WhoCraft/TardisRefined/issues/377)
- Bug fix: tardis is damaged [#351](https://github.com/WhoCraft/TardisRefined/issues/351)
- Bug fix: Diagonal Windows makes it impossible to craft the terraformer [#383](https://github.com/WhoCraft/TardisRefined/issues/383)
- Bug fix: relogging causes TARDIS Dance events to not occur [#387](https://github.com/WhoCraft/TardisRefined/issues/387)
- Bug fix: [Incompatibility] Tardis refined dimensions fail to load with Dimension Threads  [#374](https://github.com/WhoCraft/TardisRefined/issues/374)
- Bug fix: Console cannot be removed/changed with the console configurator outside the TARDIS dimension  [#380](https://github.com/WhoCraft/TardisRefined/issues/380)
- Bug fix: Fixed a bug where the overlay keybinds always rendered the default key
- Bug fix: Fixed a bug where a new TARDIS would believe it was at 0,0,0
- Bug fix: Fixed a bug where users would be burned alive when using temperature mods
- Bug fix: [Incompatibility] Shearing Tardis crashes the game with Valkyrien Skies installed [#324](https://github.com/WhoCraft/TardisRefined/issues/324)

#### Enhancements
- Enhancement: Added Adventure Mode
- Enhancement: Standing in a Crashed smoke of a crashed TARDIS will cause 0.5 damage to the player for the duration their standing in it
- Enhancement: Recovery Progress of crashed TARDIS now displayed on controls until repair is complete
- Enhancement: Recovery Progress of crashed TARDIS is now displayed on Key tooltip
- Enhancement: Holographic exteriors on consoles now spin according to throttle
- Enhancement: Shell Viewer/Time Vortex (Accessed Via Monitor Screen)
- Enhancement: Speed up downwards descent for Gravity Shaft
- Enhancement: Improved UI for Gravity Shaft
- Enhancement: Colored various texts on Key item
- Enhancement: Bulkhead doors now have some variants, changed via the Pattern Manipulator
- Enhancement: Alarm now sounds when Fuel is below 5% and the TARDIS is not fueling
- Enhancement: Fixed Coral Hum sound not looping as intended

#### Additions
- Added Item: Mallet
- Added Villager: Pilot  (POI: Console)
- Added Interior: Useable Terraformed
- "Added" Shell: Half Baked
- Added Vortex: Clouds
- Added Vortex: Flow
- Added Vortex: Space
- Added Vortex: Waves
- Added Vortex: Stars
- Added Vortex: Twilight Glow
- Added Vortex: Aurora Dreams
- Added Vortex: Desert Mirage
- Added Vortex: Neon Pulse
- Added Vortex: Ocean Breeze
- Added Vortex: Solar Flare
- Added Vortex: Crystal Lagoon
- Added Vortex: Velvet Night
- Added Vortex: Candy Pop
- Added Vortex: Emerald Forest
- Added Vortex: LGBT Rainbow
- Added Vortex: Transgender Flag
- Added Vortex: Bisexual Flag
- Added Vortex: Lesbian Flag
- Added Vortex: Non-Binary Flag
- Added Vortex: Agender Flag
- Added Vortex: Gay Flag

#### Textures, Models & Animations
- Texture: Updated all Factory Console Variants
- Model: Updated Coral Console Model
- Model: Updated Victorian Console Model
- Model: Updated Factory Console Model
- Model: Updated Big Ben Interior Model
- Model: Updated Pathfinder Interior Model
- Animation: Updated Factory Console Flight Animation
- Animation: Updated Factory Console Idle Animation
- Animation: Added Factory Console Crash Animation
- Animation: Added Factory Console Power on Animation
- Animation: Added Factory Console Power off Animation
- Animation: Updated Victorian Console Flight Animation
- Animation: Updated Victorian Console Idle Animation
- Animation: Added Victorian Console Crash Animation
- Animation: Added Victorian Console Power on Animation
- Animation: Added Victorian Console Power off Animation

#### Adventure Mode
Mod Pack creators can now enable adventure mode in the server config - this will activate a mode where players have to visit a dimension and sample it in order to have their TARDIS travel there - Mod Pack creators can also add levels to automatically be sampled by a TARDIS

#### Compatibility Notes
- [Trinkets](ExtendedInventoryMods.md#trinkets)
- [Curios](ExtendedInventoryMods.md#curios)
- [Diagonal Windows](Diagonal-Blocks-Windows-Walls.md)
- [](ValkyrienSkies.md)


#### Technical changes
- Most animations for Consoles are now loaded from JSON
- Some models for Consoles are now loaded from JSON

#### NOTE
- Upon updating to this version, your previous: ``Return Location``, ``Current Location`` and ``Target Location`` will be reset
  This will not lead to any other data loss, and your TARDIS will be exactly where you left it, take off once and you will be all sorted. This was a required change to resolve some issues

### Special Thanks
Can't do it all ourselves, can we?

#### Edrax 
- Vortex Rendering
- User interface rendering

#### MuttDud
- Fixed Coral Hum sound not looping as intended

#### River Thomas & Govert 
- [Valkyrien Skies Compatibility](ValkyrienSkies.md)

#### Lucraft
- Assistance with JSON Model Loader

#### nanuwo
- Fix blockstates being incorrect when attempting to render Astral Manipulator recipes



