### Mohist.yml

The file path `*/mohist-config/mohist.yml`

* `entity-tick-limit: 300`

* `hidejoinmodslist: false`  
  #: 隐藏玩家进入服务器在控制台显示的模组列表

* `world`  
  #: 与world有关的设置
  - `directory_in_client: true`  
    #: 世界储存路径安装客户端进行  
  - `stopserversaveworlds: false`  
    #: 服务器关闭时不保存所有世界
  - `dimensionsNotLoaded: []`  
    #: 该列表中的维度ID将不会被服务器加载

* `mohist`
  - `use_custom_java8: false`  
    #: 设置为`true`后你可以使用自定义版本的JAVA8
  - `check_update: true`  
    #: Mohist版本更新检测
  - `server-type: FML`  
    #: 设置客户端MOTD右下角显示的图标， 可设置为 `FML` `BUKKIT` `VANILLA`
  - `lang: xx_XX`  
    #: 控制台与内部提示的语言，默认使用系统语言
  - `console_name: Server`  
    #: 使用控制台发送信息时显示的前缀名
  - `CloseChatInConsole: false`  
    #: 开启后玩家在服务器所有的发言将不会显示在控制台，但仍会被记录到log中
  - `check_libraries: true`  
    #: 检测运行所需的库，如果不存在将自动下载
  - `support_nocmd: false`  
    #: 部分使用面板服的需要开启该设置
  - `disable_mods_blacklist: false`  
    #: 关闭mods黑名单检测，大部分都是不兼容或者已经在mohist内部实现的mod
  - `disable_plugins_blacklist: false`  
    #: 关闭插件黑名单检测，大部分都是不兼容或者已经在mohist内部实现的插件
  - `check_update_auto_download: false`  
    #: 检测到新版本后自动下载
  - `realtimeticking: false`  
    #: realtime？ 该功能来自SpongeForge
  - `watchdog_mohist: false`  
    #: Mohist的watchdog
  - `watchdog_spigot: true`  
    #: Spigot的watchdog
  - `showlogo: true`  
    #: 运行Mohist时你会看到的字符LOGO
