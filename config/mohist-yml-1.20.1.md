### Mohist.yml

The file path `*/mohist-config/mohist.yml`

* `mohist`    
  #: Mohist related options
    - `check_update: true`    
      #: Enabling / Disabling update checker. Set `true` to enable, `false` to disable.

    - `lang: xx_XX`   
      #: The language of the console and internal prompts, the system language is used by default. Set `fr_FR` for french, `ru_RU` for russian and `zh_CN` for chinese. Default language is english.

    - `check_libraries: true`   
      #: Enabling / Disabling libraries checker. Set `true` to enable, `false` to disable

    - `libraries_downloadsource: MOHIST`   
      #: Provide 3 options: MOHIST, CHINA, GITHUB

* `libraries_black_list: []`    
  #: When you fill this, you can make a specific library not downloaded by libraries checker. add `filename1` for example.  
  #: Can also be used to fix JarJar module conflicts  
     Example: When starting the server it crashes and gives: Exception in thread "main" java.lang.module.ResolutionException: Module smartbrainlib reads more than one module named org.yaml.snakeyaml  
     At this time, we can add the jar name of the org.yaml.snakeyaml module to the list
     ```
     libraries_black_list:
        - "snakeyaml-2.0"
     ```

* `player_modlist_blacklist:`    
    #: Built-in modid blacklist
    - `enable: false`    
      #: Used to enable / disable the mod blacklist, set to `false` by default (boolean).
    - `list: []`    
      #: Mod ID array. Enter the MODID's of the mods you want to disable.    
      #: If enabled, the layout changes after the `server.jar` is restarted    
      > Before restart:
      ```
      player_modlist_blacklist:
        enable: true
        list ["examplemodid"]
      ```
      > After restart:
      ```
      player_modlist_blacklist:
        enable: true
        list:
        - examplemodid
      ```
