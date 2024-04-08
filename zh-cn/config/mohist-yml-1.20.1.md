### Mohist.yml

文件位于路径 `*/mohist-config/mohist.yml`

* `mohist`
  #: 与Mohist相关的配置项 
    - `check_update: true`
      #: 启用/禁用更新检查器。设置`true`以启用，`false`以禁用。

    - `lang: xx_XX` 
      #: 控制台和内部提示的语言，默认使用系统语言。设置`fr_FR`为法语，`ru_RU`为俄语，`zh_CN`为中文。默认语言是英语。

    - `check_libraries: true` 
      #: 启用/禁用运行库检查器。设置`true`以启用，`false`以禁用。

    - `libraries_downloadsource: MOHIST` 
      #: 运行库下载源，提供3个选项：MOHIST，CHINA，GITHUB。

* `libraries_black_list: []`
  #: 填写此项时，你可以使特定的运行库不被运行库检查器下载。例如，添加`filename1`。
  #: 还可以用来解决JarJar模块冲突。
     示例：当启动服务器时，出现崩溃并给出错误：```线程"main"中的异常 java.lang.module.ResolutionException：模块smartbrainlib读取了一个以上名为org.yaml.snakeyaml的模块```
     此时，我们可以将org.yaml.snakeyaml模块的jar名称添加到列表中
     ```
     libraries_black_list:
        - "snakeyaml-2.0"
     ```

* `player_modlist_blacklist:`
    #: 内置的 modid 黑名单
    - `enable: false`
      #: 用于启用/禁用 mod 黑名单，默认设置为`false`（布尔值）。
    - `list: []`
      #: Mod ID 数组。输入你想要禁用的 mod 的 MODID。
      #: 如果启用，`server.jar`重启后配置文件布局会改变
      > 重启前:
      ```
      player_modlist_blacklist:
        enable: true
        list ["examplemodid"]
      ```
      > 重启后:
      ```
      player_modlist_blacklist:
        enable: true
        list:
        - examplemodid
      ```
···
