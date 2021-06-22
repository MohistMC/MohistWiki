## Mohist Commands
---

> All commands made by Mohist are listed here.    

**Important**: This command list can be different depending to your Mohist version (1.12.2 or 1.16.5). A command here can be unavailable on a version but will be implemented soon.

---

* `/mohist [mods|playermods|printthreadcost|lang|item|reload|give]`   
    Permission: *mohist.command.mohist*

    Argument `mods`: Give server mod list   
    Argument `playermods`: Give a player mod list (need a second argument)  
    Argument `printthreadcost`: Print the Mohist thread cost.  
    Argument `lang`: Give the current Mohist language.  
    Argument `item`: Give the information about a block/item (you need to execute this command with a block/item in your hand)  
    Argument `reload`: Reload Mohist config file.  
    Argument `give`: Give command which works with modded blocks/items.

---

* `/backupworld <worldname>`    
    Permission: *mohist.command.backupworld*

    This command enables you to create a zip file of your world while server is running without freezing the server.

---

* `/downloadfile <filename> <path> <url>`   
    Permission: *mohist.command.downloadfile*

    This command enables you to download a file from internet. To use it you need to set `downloadfile_command_enabled` to `true` in `mohist.yml`
    > Disclaimer: Don't let unknown people use this command!

---

* `/dump <file|web> [potions|enchants|cbcmds|modscmds|entitytypes|biomes|pattern|worldgen|worldtype|bukkit_material|vanilla_material]`   
    Permission: *mohist.command.dump*

    This command will dump something you want in the available args. This can be given into 2 ways: Web (hastebin) or in a file.

---

* `/entity [reload|dump-existing]`    
    Permission: *mohist.command.entity*

    Argument `reload`: Reload `entities.yml` config file
    Argument `dump-existing`: Update `entities.yml` with found entities

---

* `/getmodlist`    
    Permission: *mohist.command.getmodlist*   

    This command will paste your mod list will all details into a hastebin page. It will return you the url when it's done.

---

* `/getpluginlist`    
    Permission: *mohist.command.getpluginlist*    

    This command will paste your plugin list will all details into a hastebin page. It will return you the url when it's done.

---

* `/plugin [load|unload|reload] [name]`    
    Permission: *mohist.command.plugin*

    Argument `load`: Load a plugin
    Argument `unload`: Unload a plugin
    Argument `reload`: Reload a plugin
    Argument `name`: The plugin name

    This command enables you to load, unload or reload a specific plugin.

---

* `/whitelistmods [enable|disable|update]`    
    Permission: *mohist.command.whitelistmods*

    Argument `enable`: Enable to mods whitelist
    Argument `disable`: Disable the mods whitelist
    Argument `update`: Update the mod list automatically in mohist.yml with server mods

    This command is a feature from `mohist.yml` which enables to you to only allow certain mods on your server. When the `enable` argument is specified, the list will be automatically filled with server mod list. You can manually edit the allow mod list in the `mohist.yml` file.