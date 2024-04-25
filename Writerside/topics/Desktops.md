# Desktops

Through the use of Datapacks, it is possible to implement custom desktops which can be taken from the save file and reused in other areas.

## Datapack Work


### Requirements
In order to create desktop, there are only two requirements.

1. The TARDIS Door
2. The Airlock Generator

```
/give @p tardis_refined:air_lock_generator
```

The Airlock Generator will place the airlock upon generating the desktop. It will be placed SOUTH of the block.

![desktop_basic_structure.png](desktop_basic_structure.png)


### Desktop Export Command

As a handy tool, we have provided the following command. This command will generate all the required datapack files for a new desktop, and automatically load it into the datapack folder of the world save so you don't have to!

```
/tardis_refined data export desktop <X1> <Y1> <Z1> <X2> <Y2> <Z2> <include_entities> <name_space> <desktop_id> <datapack_name> <display_name>
```

``X1, Y1, Z1``
: A BlockPos, the first corner of the built structure.

``X2 Y2 Z2``
: A BlockPos, the direct opposite corner of the built structure.

``include_entities``
: True or False, Includes saving entities in the structure. Can be useful for if item frames or armor stands are present in the build.

``name_space``
: String, The namespace of the datapack.
: Examples: ``tardis_refined_tweaks``, ``panda``

``desktop_id``
: String, Unique identifier for the desktop.
: Examples: ``neon``, ``hartnell_lounge``

``datapack_name``
: String, Name of the datapack.
: Examples: ``cool_pack``, ``custom_name_here``

``display_name``
: NBTComponent, Display Text for the UI.
: ONLY USE the Minecraft Tellraw generated text, DO NOT include the tellraw command syntax. <a href="https://www.minecraftjson.com/">You can find a generator here.</a>
: Example: ``{\"color\":\"gold\",\"text\":\"Copper\"}``

## Resource Pack
### Desktop Preview Texture
By default, the desktop preview texture will show a placeholder texture. If you want to show a texture for the desktops, you need to create a Minecraft Resource Pack that follows the following structure:

```
* assets
    * [your_resource_pack_namespace]
        * textures
            * ui
                * desktops
                    * [your_desktop_id].png
```

>Note: It is very important that this EXACT folder structure is used, because Tardis Desktops will only look from this exact type of folder structure.
> 
> {style="warning"}