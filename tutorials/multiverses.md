## How to have multiple worlds with Mohist?
---

⚠️ **Disclaimer: To have multiple worlds with Mohist you can't use Multiverse or other plugin alternatives since they don't work well with forge and mods.**

### -> Steps to create new worlds in 1.12.2: 

* Download [this mod](https://www.curseforge.com/minecraft/mc-mods/just-enough-dimensions) and put it in your "mods" folder.

* Start your server and stop it after it completely loaded to generate the config file.

* To create a new simple world you can use [this preset (dimensions.json)](https://cdn.discordapp.com/attachments/815331146303799296/825439539438157904/dimensions.json), download it and put it inside "config/justenoughdimensions" and then use /tpj 2 to teleport to this world. To create other worlds use the same syntax than the preset and change the dimension ID (You can't have the same dimension ID for more than one dimension).

<details>
  <summary>Main options</summary>
  
    - "dim" : Should be the same than the dimension ID.
  
    - "load_on_start" : set it to true if you want your dimension to be loaded at the start of your server (should be always enabled to not cause issues with plugins).
  
    - "keeploaded" :  set it to false if you want your dimension to be unloaded if there is no players inside.
  
    - "id" : This is the dimension ID  (Remember that you can't have the same dimension ID for more than one dimension).
  
    - "name" : The name of the dimension (only used by forge mods.)
  
    - "worldprovider" : Type of the dimension ("WorldProviderSurface" for an overworld type world, WorldProviderHell  for a nether type world and WorldProviderEnd for a end type world. you can also use worldproviders from mods if you know them !)
  
    - "require_exact_match" : should be always present and set to true.
    
There is other settings that you can set, you can see them in the mod's curseforge page.
</details>

<details>
  <summary>Preset Json</summary>
  
```json
{
  "config_version": {
    "id": "__default",
    "version": 0
    },
    "dimensions":
    [
        {
            "dim": 2,
            "load_on_start": true,
            "dimensiontype": {
                "id": 2,
                "name": "AltWorld",
                "keeploaded": true,
                "worldprovider": "WorldProviderSurface",
                "require_exact_match": true
            }
        }
    ]
}
```
</details>

### -> Steps to create new worlds in 1.16.5+: 

* Download [this datapack](https://cdn.discordapp.com/attachments/615256015704948808/850816329636380752/multiworld.zip) and extract it in world/datapacks folder.

* Start your server and use the command /execute in multiworld:altworld-1 run tp ~ ~ ~ to teleport yourself in the new world (work also with plugins commands).

* If you need more world, you need to copy and paste the .json inside world/datapacks/multiworld/data/multiworld/dimension and rename it (eg: altworld-3.json).

<details>
  <summary>Datapack Json</summary>
  
```json
{
  "type": "minecraft:overworld",
  "generator": {
    "type": "minecraft:noise",
    "seed": 0,
    "biome_source": {
      "type": "minecraft:vanilla_layered",
      "seed": 0,
      "large_biomes": false
    },
    "settings": "minecraft:overworld"
  }
}
```
</details>

### -> Steps to create new worlds in 1.20.1+:

    Use the Multiverse-Core plugin directly Or directly use the /worlds command that comes with mohist
