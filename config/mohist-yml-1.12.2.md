### Mohist.yml

The file path `*/mohist-config/mohist.yml`

* `entity-tick-limit: 300`

* `hidejoinmodslist: false`  
  #: Hide the player's mod list

* `world`  
  #: World-related settings
  - `directory_in_client: true`  
    #: Install the client to the world storage path
  - `stopserversaveworlds: false`  
    #: Do not save all worlds when the server is shut down
  - `dimensionsNotLoaded: []`  
    #: The dimension IDs in this list will not be loaded by the server

* `mohist`
  - `use_custom_java8: false`  
    #: After setting to `true` you can use a customized version of JAVA8
  - `check_update: true`  
    #: Mohist version update detection
  - `server-type: FML`  
    #: Set the icon displayed in the lower right corner of the client MOTD, which can be set to `FML` `BUKKIT` `VANILLA`
  - `lang: xx_XX`  
    #: The language of the console and internal prompts, the system language is used by default
  - `console_name: Server`  
    #: The prefix name displayed when sending information using the console
  - `CloseChatInConsole: false`  
    #: After opening, all the speeches of the player on the server will not be displayed in the console, but will still be recorded in the log
  - `check_libraries: true`  
    #: Check the library required for operation, if it does not exist, it will be downloaded automatically
  - `support_nocmd: false`  
    #: Some people who use panel servers need to enable this setting
  - `disable_mods_blacklist: false`  
    #: Turn off mods blacklist detection, most of them are incompatible or mods that have been implemented inside mohist
  - `disable_plugins_blacklist: false`  
    #: Turn off plugins blacklist detection, most of them are incompatible or plugins that have been implemented inside mohist
  - `check_update_auto_download: false`  
    #: Automatically download when new version is detected
  - `realtimeticking: false`  
    #: realtime game running (instead of game ticking). This feature comes from SpongeForge
  - `watchdog_mohist: false`  
    #: Mohist's watchdog
  - `watchdog_spigot: true`  
    #: Spigot's watchdog
  - `showlogo: true`  
    #: The character LOGO you will see when running Mohist
