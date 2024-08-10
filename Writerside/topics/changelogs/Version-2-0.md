# Version 2.0

![tardis_refined_v2.png](tardis_refined_v2.png)

## NEW FEATURES

+ Added Astral Manipulator crafting.
+ Added Interior Ambiance.
+ Added Fuel and Power.
+ Added Eye of Harmony.
+ Added Infinite Corridors.
+ Added System Upgrades.
+ Added TARDIS XP.
+ Reworked Flight System.
+ Added Waypoint saving.
+ Added Amethyst Screwdriver.
+ Added Gravity Wells.
+ Added Corridor Teleporters.
+ Added new shells.
+ Added new desktops.

### ASTRAL MANIPULATOR CRAFTING
+ The Astral Manipulator is a new crafting block.
+ Recipes are placed in the world as blocks.
+ Crafting region is selected with new Amethyst Screwdriver.
+ All device crafting recipes have been replaced with this new system.

### FLIGHT CHANGES
+ Added throttle to control flight speed.
+ Added handbrake.
+ Flight progress can be seen by looking at the Computer Bank control.
+ Flight can end early, landing at the percentage of the flight completed.
+ Flight events are no longer required for flights to be completed.
+ Flight events now can fall out of alignment, requiring the player to set them right.
  + Their status can be seen in the colour of the icon next to the control name.
+ Controls that are misaligned for too long will become damaged and will no longer be usable until flight is over.
+ Too many misaligned controls will cause the TARDIS to crash.
+ AR Glasses allow the player to see more obviously what controls are out of line, reusing the original particles!


### FUEL AND POWER
+ The TARDIS requires fuel to fly.
+ The TARDIS cannot take off until the Eye of Harmony has been activated.

### EYE OF HARMONY
+ New room under the corridor hub
+ Contains a portal that has to be opened for the TARDIS to fly.
+ Requires building four artron pillars and crafting them in place to activate.

### INTERIOR AMBIANCE
+ Hums have been added to the TARDIS dimension.
+ Hums can be changed in the Computer Bank.
+ Hums can be added with a datapack.

### INFINITE ROOMS & CORRIDORS
+ Corridors and rooms now generate from the corridor hub.
+ There are two layers of corridors.
+ Rooms are empty, ready to be filled.
+ Every 6 chunks a gravity shaft chamber generates with teleporters to return to the hub.

### SYSTEM UPGRADES & TARDIS XP
+ Some TARDIS features are now locked by a progression system. 
+ Upgrades can be unlocked by gaining TARDIS experience levels, which create points.
    + Increased increments: 1000, 2500, 5000
    + Dimension swapping
    + Chameleon Circuit
    + Desktop changing
    + Landing pad summoning
    + Landing on people teleports them inside
    + Waypoint saving
    + Desktop switching times - 120 seconds, 60 seconds and 10 seconds.

### WAYPOINTS
+ Allows for locations to be recorded onto the TARDIS
+ Waypoint creation takes the target position for saving

### EXTERIOR SHELLS
+ Updated Police Box Shell model
+ Updated Factory Shell model
+ Added Lift Shell
+ Added Hieroglyph
+ Added Castle
+ Added Pathfinder

### DESKTOPS
+ Added "Refurbished" - based on the new Desktop from the 2023 Specials
+ Added "Arnet" - ported Desktop from The Master's Delight 

### COMMANDS
+ Added upgrade sub-command

## CHANGES

+ Desktop generation now takes 180 seconds by default.
+ Added Destination Reached “Ding” noise. This plays when the TARDIS initially starts landing
+ Players must now use Shears to unlock the growth stage TARDIS
+ Corridor hub has been completely reworked, allowing for more areas to be modified 
+ Terraformer now requires to be right-clicked by the Amethyst Screwdriver
+ Shell animations now play in the Shell selection screen
+ Interior doors and Shells now hold their own data instead of taking it from their related dimension
+ Initial generation code optimized to be less noticeable
+ Crashed TARDIS now emits smoke particles as if room is overflowing with smoke
+ Root Plant now emits particles when growing to indicate to the user that they are doing it correctly
+ Landing Pad is now locked behind upgrades
+ Added ARS Leaves Particles (currently using the Cherry Leaf)
+ Bulkhead doors can now be crafted
+ Fixed bug where users could not leave via Immersive-Portals-portals due to a portal sizing issue
+ Interior doors and Shells now hold their own data instead of taking it from their related dimension
+ Sounds that loop are now handled differently, improving performance
+ Root shell now only creates the TARDIS dimension when sheared (Significantly increases performance)
+ Non-player entities can now teleport into the TARDIS
+ Entity facings are now preserved when teleporting into the TARDIS
+ Console Units no longer spawn their controls if not in a TARDIS
+ A TARDIS can only have one main console unit, but can be changed by right-clicking another unit
+ Console Units can be destroyed in creative when they're not in a TARDIS dimension
+ Optimized landing calculations

## API
### ADDITIONS
- Added TARDIS Upgrade Unlocked Event
- Replaced use of Enums with custom registries for: Shells, Patterns, Desktops, Consoles, Upgrades. This allows other mods to add new entries without needing mixins.
+ Shell pattern datapacks no longer hardcode the datapack namespace to tardis_refined
+ Shell pattern datapacks now allow replacement of other shell patterns by specifying a “replace” field to “true”.
