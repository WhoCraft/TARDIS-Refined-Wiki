# Valkyrien Skies

Valkyrien Skies adds physics to Minecraft, which brings with it some fantastic opportunities for a Tardis. However, it also brings some big changes under the hood. Tardis Refined has mostly been made compatible, but beware some problems you may run into.

First, we'll go over what the compatibility adds, then list some things to avoid, followed by a quick FAQ.

## Compatibility

- As of Tardis Refined 2.1.0, Minecraft no longer crashes when shearing the Tardis while having VS installed!
- A Tardis can be part of a VS Ship, either by assembling a Ship with the Tardis connected, by growing it on a Ship, or by landing on a Ship
- To remove the Tardis from a Ship, a Tardis can take off from a Ship, or be disassembled from a Ship
- To land a Tardis on a VS Ship, simply fly to the expected coordinates as you normally would, and if there's a Ship, the Tardis will try to land on it instead
- The Tardis can be part of other VS compatible contraptions, like Create Trains with the Create Interactive addon
- The Tardis will show correct world data on the monitor
- If a Ship moves while you're inside the Tardis, the monitor will update your location in realtime
- The Tardis will also show correct data on other compatible displays, like Create displays using the Create Display Link
- Ships can be created inside the Tardis. This includes VS compatible contraptions, like Create Interactive entities
- The inner Tardis doors can be placed on and moved by a Ship, even while entering/exiting the Tardis
- The Astral Manipulator can be used on a Ship
- Use a Landing Pad to summon the Tardis to a Ship
- Works with multiplayer

## A few things to watch out for

- Due to the way the airlock works, it is not possible to move them with a VS Ship. Note that moving the surrounding blocks or doors will not move the airlock.
- We recommend not moving the console. Button hitboxes *will not* move with the Ship, and Shippifying the console while in flight causes known issues. This will be fixed in a future version. That said, moving inactive consoles is possible, though also not recommended.
- Ships do not fly through the Tardis doors. This is an intentional choice - while the inside may be bigger than the outside, the doorframe is not!

## Further questions

1. **What's with all the "Ship" references? Does it only work on water?** Valkyrien Skies calls any moving entity a *Ship*. For consistency, we use the word "Ship" on this page, but the moving entity can be anything - a train, plane, or even a hot air balloon. You can be the Next Doctor with your very own Tardis (Tethered Aerial Release Developed In Style)!
2. **What about Valkyrien Skies addons?** Some have been tested, like `Create Interactive`, `Clockwork`, and `Eureka!`. Support for others isn't guaranteed, but there's a pretty good chance it'll work.
3. **Does this also work with other mods that could move the shell?** While some may work, our goal is to provide compatibility with Valkyrien Skies and its addons. Any other mods are at your own risk, and may break the Tardis.
4. **Help, I'm seeing weird, large, coordinates?** Not to get too technical, but Valkyrien Skies stores the blocks that form ships far away from the spawn, including the Tardis shell. While the compatibility should automatically translate those to the expected coordinates, sometimes you may see them pop up on the screen. Don't worry, you haven't suddenly moved to a galaxy far far away, the Ship with the Tardis is right where you left it, the UI just hasn't caught up yet.
5. **I want to remove Valkyrien Skies, will my Tardis still be there?** If you remove Valkyrien Skies, make sure to disassemble any ships first, or at least move the Tardis off of any ship. Valkyrien Skies may show ships flying around the overworld, but the blocks are stored millions of blocks away. That's where the Tardis would end up if it's still attached to a ship when uninstalling Valkyrien Skies!
6. **If Valkyrien Skies stores Ships so far away, won't that affect fuel and flight time?** When Shipyard coordinates are detected, they automatically get converted so flight duration and fuel cost don't get out of control.

### Valkyrien Skies
> [Website](https://www.valkyrienskies.org/)

> [CurseForge](https://www.curseforge.com/minecraft/mc-mods/valkyrien-skies)

> [Modrinth](https://modrinth.com/mod/valkyrien-skies)
