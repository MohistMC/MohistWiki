### Mohist.yml

文件位于路径 `*/mohist-config/mohist.yml`

* `mohist`
  #: Mohist 相关的配置项 
  - `check_update: true`
    #: 启用/禁用更新检查。设置`true`来启用，`false`来禁用。

  - `lang: xx_XX` 
    #: 控制台和内部提示的语言，默认使用系统语言。设置`fr_FR`表示法语，`ru_RU`表示俄语，`zh_CN`表示中文。默认语言是英语。

  - `custom_flags: aaaa bbbb` 
    #: 您可以在这里使用自定义 jvm 参数，比如 Aikar 参数。填写方式如`anarg anotherarg`。

  - `check_libraries: true` 
    #: 启用/禁用运行库检查器。设置`true`来启用，`false`来禁用。

  - `libraries_downloadsource: MOHIST` 
    #: 运行库下载源，提供三个选项：MOHIST，CHINA，GITHUB。

  - `disable_mods_blacklist: false` 
    #: 关闭模组黑名单检测，大部分是不兼容的或已在Mohist内部实现的模组。设置`true`来启用，`false`来禁用。

  - `disable_plugins_blacklist: false`
    #: 关闭插件黑名单检测，大部分是不兼容的或已在Mohist内部实现的插件。设置`true`来启用，`false`来禁用。

  - `check_update_auto_download: false` 
    #: 检测到新版本时自动下载。设置`true`来启用，`false`来禁用。

  - `use_custom_java11: false`
    #: 如果您的电脑未安装 Java 11 或低于 Java 16 的版本，将此设置为`true`将自动下载 Java 11。设置`true`来启用，`false`来禁用。

  - `showlogo: true`
    #: 在服务器启动时显示 Mohist logo。设置`true`来启用，`false`来禁用。

  - `optimize_explosions: true` 
    #: 优化爆炸，这是来自 Paper 的功能。设置`true`来启用，`false`来禁用。

  - `prevent_from_entering_unloaded_chunks: true` 
    #: 设置为`true`以禁止玩家进入正在生成/加载的区块（区块未准备好）。设置为`false`以停止此检查（不推荐，如果玩家继续进入未加载的区域，可能会导致级联延迟）。

  - `forge_ignore_optional_mods_version_check: false` 
    #: 忽略 Forge 模组版本检查。如果某个模组的兼容性没有被正确检测到，这可能会很有用。设置`true`来启用，`false`来禁用。

  - `ignore_empty_time: all_worlds` 
    #: 此选项强制始终运行一些额外的区块逻辑（例如使区块加载器能够继续工作），即使目标世界中没有玩家。`all_worlds`适用于所有已加载的世界（推荐），填入`世界名称`以对特定世界启用。

  - `chunk_unload_delay: 5` 
    #: 这里的5是区块卸载前的不活动时间（以秒为单位）。5秒是最佳选项，如果您想要极其安全的区块卸载，可以调整为10秒。

* `forge` 
  #: Forge 相关的配置项
  * `modsblacklist` 
  #: 模组黑名单
    - `enable: false` 
        #: 启用或禁用模组黑名单。设置`true`来启用，`false`来禁用。

    - `list: aaaa,bbbb` 
        #: 放置您希望禁止的模组列表。例如，设置为`xray`或`xray,anothermod`。您必须使用 modid 填写！

    - `kickmessage: Use of unauthorized mods` 
        #: 自定义玩家使用未授权的模组加入服务器时的踢出信息。

  * `modswhitelist` 
  #: 模组白名单
    - `enable: false` 
       #: 启用或禁用模组白名单。设置`true`来启用，`false`来禁用。

    - `mods_number: 0`
       #: 填入允许的模组数量。如果客户端的模组数量超过此数值，将会被断开连接。例如，设置`1`来只允许`1`个模组。

    - `list: minecraft,forge` 
       #: 填入您希望允许在您的服务器上使用的模组列表。您可以使用`/whitelistmods enable`或`/whitelistmods update`来自动更新这个列表。

    - `kickmessage: Use of unauthorized mods` 
       #: 自定义玩家使用未授权的模组加入服务器时的踢出信息。

 * `hidejoinmodslist: false`
 #: 当客户端加入服务器时，在控制台中隐藏模组信息。设置`true`来启用，`false`来禁用。


* `consolecolor`
  #: 控制台色彩相关的配置项
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
  #: 当您填入此配置时，您可以让特定的运行库不被运行库检查器下载。例如，设置`filename1`或`filename1,filename2`。
