### Mohist.yml

The file path `*/mohist-config/mohist.yml`

* `mohist`    
  #: Mohist related options
  - `check_update: true`    
    #: Enabling / Disabling update checker. Set `true` to enable, `false` to disable.

  - `lang: xx_XX`   
    #: The language of the console and internal prompts, the system language is used by default. Set `fr_FR` for french, `ru_RU` for russian and `zh_CN` for chinese. Default language is english.

  - `custom_flags: aaaa bbbb`   
    #: You can use custom flags here like Aikar flags. Fill like this `anarg anotherarg`.

  - `check_libraries: true`   
    #: Enabling / Disabling libraries checker. Set `true` to enable, `false` to disable

  - `disable_mods_blacklist: false`   
    #: Turn off mods blacklist detection, most of them are incompatible or mods that have been implemented inside mohist. Set `true` to enable, `false` to disable

  - `disable_plugins_blacklist: false`    
    #: Turn off plugins blacklist detection, most of them are incompatible or plugins that have been implemented inside mohist. Set `true` to enable, `false` to disable

  - `check_update_auto_download: false`   
    #: Automatically download when new version is detected. Set `true` to enable, `false` to disable

  - `use_custom_java11: false`    
    #: If you don't have java 11 or a version under java 16 installed on your pc, setting this to true will download java 11 automatically. Set `true` to enable, `false` to disable

  - `showlogo: true`    
    #: Show Mohist logo at server start. Set `true` to enable, `false` to disable

  - `optimize_explosions: true`   
    #: Optimize explosions, a feature comes from paper. Set `true` to enable, `false` to disable

  - `prevent_from_entering_unloaded_chunks: true`   
    #: Set `true` to enable, `false` to disable

  - `forge_ignore_optional_mods_version_check: false`   
    #: Ignore forge mods version check. Can be useful if a compatibility of a mod isn't detected correctly. Set `true` to enable, `false` to disable

  - `ignore_empty_time: all_worlds`   
    #:
  - `chunk_unload_delay: 5`   
    #:

* `forge`   
  #: Forge related options
  * `modsblacklist`   
  #: Mods blacklist
    - `enable: false`   
        #: Enable or disable the mods blacklist. Set `true` to enable, `false` to disable

    - `list: aaaa,bbbb`   
        #: Put the list of the mods you want to disallow. Set `xray` or `xray,anothermod` for example. You must fill with modid !

    - `kickmessage: Use of unauthorized mods`   
        #: Customize kick message when use join with unauthorized mods.

  * `modswhitelist`   
  #: Mods whitelist
    - `enable: false`   
       #: Enable or disable the mods whitelist. Set `true` to enable, `false` to disable

    - `mods_number: 0`    
       #: Put the mods number authorized. If a client have more than this number, it will be disconnected. Set `1` to only allow 1 mod for example.

    - `list: minecraft,forge`   
       #: Put the list of the mods you want to allow on your server. You can use `/whitelistmods enable` or `/whitelistmods update` to update this list automatically

    - `kickmessage: Use of unauthorized mods`   
       #: Customize kick message when use join with unauthorized mods. Set `true` to enable, `false` to disable

 * `hidejoinmodslist: false`    
 #: Hide mods in the console when a client joins the server. Set `true` to enable, `false` to disable


* `consolecolor`    
  #: Options related to console colors.
  - `info-time: b`
  - `info-level: 2`
  - `info-msg: r`
  - `warn-time: e`
  - `warn-msg: e`
  - `warn-level: e`
  - `trace-level: c`
  - `fatal-time: c`
  - `error-level: c`
  - `error-msg: c`
  - `fatal-msg: c`
  - `error-time: c`
  - `trace-time: c`
  - `fatal-level: c`
  - `trace-msg: c`

* `libraries_black_list: aaaaa;bbbbbb`    
  #: When you fill this, you can make a specific library not downloaded by libraries checker. Set `filename1` or `filename1,filename2` for example.