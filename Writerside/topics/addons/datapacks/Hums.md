# Hums

Through the use of Datapacks, it is possible to implement custom soundscapes! (Also known as "Hums")

## Requirements
- A Resource Pack
- A Data Pack

## Resource Pack
Within your resourcepack, create custom sounds, you can learn how to do this [here](https://youtu.be/VIt0JsFklZI)

Once you have completed this step, you are done with the resource pack side of things!

## Data Pack

### File Structure
Console patterns follow the following structure:
```
* data
    * [your_datapack_pack_namespace]
        * tardis_refined
                * hums
                    * [hum_name].json
```


Here is an example entry from the mod, you may edit to your needs!

```JSON
{
  "ambient_sounds": [
    "minecraft:ambient.crimson_forest.additions",
    "minecraft:ambient.crimson_forest.mood"
  ],
  "hum_sound": "minecraft:ambient.crimson_forest.loop",
  "id": "tardis_refined:crimson_forest",
  "name_component": "{\"color\":\"gold\",\"text\":\"Crimson Forest\"}"
}
```

``ambient_sounds``
: An array of sounds that will play at randomly and not continuously

``hum_sound``
: One sound entry that will play on a loop forever until the player changes hum

``id``
: String, Unique identifier for the hum.
: Examples: ``bables``, ``the_forbidden_lands``

``name_component``
: NBTComponent, Display Text for the UI.
: ONLY USE the Minecraft Tellraw generated text, DO NOT include the tellraw command syntax. <a href="https://www.minecraftjson.com/">You can find a generator here.</a>
: Example: ``{\"color\":\"gold\",\"text\":\"The Forbidden Lands!\"}``

