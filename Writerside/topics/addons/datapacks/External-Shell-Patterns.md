# Shell Patterns

The external shell of the Tardis can be customised in the External Shell Selection Screen, which can be accessed from the Computer Bank Control on a Tardis Console unit.

![shell_change_gui.png](shell_change_gui.png)

This feature provides users the ability to match their console with their personal preferences and style.

![shell_patterns.png](shell_patterns.png)

## Datapack

### File Structure
Shell patterns follow the following structure:
```
* data
    * [your_datapack_pack_namespace]
        * tardis_refined
            * patterns
                * shell
                    * [shell_theme_id].json
```

### Pattern JSON

Inside the datapack you need to create a ``.json`` file to define the properties of the Shell Pattern.

The name of this JSON file MUST match the name of the shell theme you are modifying. E.g. If you are modifying the Police Box Shell theme you must use its id of police_box.

> To see the list of Shell theme IDs, you can find them inside the mod's JAR file using a computer program such as 7zip. The directory inside the JAR file is data/tardis_refined/tardis_refined/patterns/shell.

The JSON structure for Shell Patterns differ slightly from that of Console Patterns, most notably, the exterior and interior fields, which define the texture for the Exterior Shell and Internal Door model respectively.

``police_box.json``
```json
{
  "patterns": [
    {
      "id": "example:police_box_green",
      "exterior": {
        "emissive": false,
        "texture": "example:textures/blockentity/shell/police_box/police_box_green.png"
      },
      "interior": {
        "emissive": false,
        "texture": "example:textures/blockentity/shell/police_box/police_box_green_door.png"
      },
      "name_component": "{\"color\":\"yellow\",\"text\":\"Green\"}"
    },
    {
      "id": "example:missing_key",
      "exterior": {
        "emissive": false,
        "texture": "example:textures/blockentity/shell/police_box/missing_key.png"
      },
      "interior": {
        "emissive": false,
        "texture": "example:textures/blockentity/shell/police_box/missing_key_door.png"
      },
      "name_component": "{\"color\":\"yellow\",\"text\":\"Missing Key\"}"
    }
  ]
  ,"replace": false
}
```

> If the ``"replace"`` field = `true`, it indicates that your patterns will replace all patterns for this Shell type.

## Resource Pack
You also need to create a Minecraft Resource Pack that contains all the textures you will be using in each pattern.

The structure of the resource pack should match what you have defined in the pattern JSON.

Example:

For instance, in the ``example:missing_key`` example of the example patterns shown above, the texture path is defined as:

``example:textures/patterns/shell/police_box/missing_key.png``
``example:textures/patterns/shell/police_box/missing_key_door.png``

This means our Resource pack that contains the texture file will need to be structured according to the full path, like so:

```
* assets
    * example
        * textures
            * patterns
                * shell
                    * missing_key.png
                    * missing_key_door.png
```

> NOTE: The image file MUST be a .png file type because Minecraft will only accept these type of image files.

### Emissive Texture Files

You can allow your Patterns to be emissive, meaning it will glow in the dark like Minecraft Glow Squids!

This is disabled by default, however you can enable it by using the following steps:

1. Inside the pattern JSON file, set the ``emissive`` field for the texture object of a Pattern to be ``true``.
2. Rename the texture file to append the word ``_emissive`` to the end. You MUST use this exact spelling or the texture won't be picked up by the mod. i.e. ``missing_key.png`` --> ``missing_key_emissive.png``
