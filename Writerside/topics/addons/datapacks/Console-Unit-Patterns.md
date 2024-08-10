# Console Unit Patterns

A console unit design can be modified by interacting with a Console Configurator on the side of a console using the Pattern Manipulator item. Users can select from a range of available patterns and designs to customize the look of their console unit.

## Datapack

### File Structure
Console patterns follow the following structure:
```
* data
    * [your_datapack_pack_namespace]
        * tardis_refined
            * patterns
                * console
                    * [console_theme_id].json
```

### Pattern JSON

Inside the datapack you need to create a ``.json`` file to define the properties of the Console Pattern.

The name of this JSON file MUST match the name of the shell theme you are modifying. E.g. If you are modifying the Copper Console theme you must use its id of copper.

> To see the list of Console theme IDs, you can find them inside the mod's JAR file using a computer program such as 7zip. The directory inside the JAR file is data/tardis_refined/tardis_refined/patterns/console.

A JSON must follow the following structure:

``copper.json``
```json
{
  "patterns": [
    {
      "id": "example:copper",
      "name_component": "{\"color\":\"yellow\",\"text\":\"Copper\"}",
      "texture_definition": {
        "emissive": false,
        "texture": "tardis_refined:textures/patterns/console/copper/copper_console.png"
      }
    },
    {
      "id": "example:sculk",
      "name_component": "{\"color\":\"yellow\",\"text\":\"Sculk\"}",
      "texture_definition": {
        "emissive": false,
        "texture": "example:textures/patterns/console/copper/copper_console_sculk.png"
      }
    }
  ]
  ,"replace": false
}
```

> If the ``"replace"`` field = `true`, it indicates that your patterns will replace all patterns for this Console Unit type.


## Resource Pack
You also need to create a Minecraft Resource Pack that contains all the textures you will be using in each pattern.

The structure of the resource pack should match what you have defined in the pattern JSON.

Example:

For instance, in the ``example:sculk`` example of the example patterns shown above, the texture path is defined as:

``example:textures/patterns/console/copper/copper_console_sculk.png``

This means our Resource pack that contains the texture file will need to be structured according to the full path, like so:

```
* assets
    * example
        * textures
            * patterns
                * console
                    * copper_console_sculk.png
```

> NOTE: The image file MUST be a .png file type because Minecraft will only accept these type of image files.

### Emissive Texture Files

You can allow your Patterns to be emissive, meaning it will glow in the dark like Minecraft Glow Squids!

This is disabled by default, however you can enable it by using the following steps:

1. Inside the pattern JSON file, set the ``emissive`` field for the texture object of a Pattern to be ``true``.
2. Rename the texture file to append the word ``_emissive`` to the end. You MUST use this exact spelling or the texture won't be picked up by the mod. i.e. ``copper_console_sculk.png`` --> ``copper_console_sculk_emissive.png``
