### Mohist.yml  
  
文件位于路径 `*/mohist-config/mohist.yml`  
  
* `entity-tick-limit: 300`  
  
* `hidejoinmodslist: false`    
  #: 隐藏玩家的模组列表  
  
* `world`    
  #: 与世界相关的设置  
  - `directory_in_client: true`    
    #: 将客户端安装到世界存储路径  
  - `stopserversaveworlds: false`    
    #: 当服务器关闭时不保存所有世界  
  - `dimensionsNotLoaded: []`    
    #: 此列表中的维度ID不会被服务器加载  
  
* `mohist`  
  - `use_custom_java8: false`    
    #: 设置为`true`后可以使用自定义版本的 Java 8  
  - `check_update: true`    
    #: Mohist 版本更新检测  
  - `server-type: FML`    
    #: 设置客户端 MOTD 右下角显示的图标，可以设置为 `FML` `BUKKIT` `VANILLA`  
  - `lang: xx_XX`    
    #: 控制台和内部提示的语言，默认使用系统语言  
  - `console_name: Server`    
    #: 使用控制台发送信息时显示的前缀名称  
  - `CloseChatInConsole: false`    
    #: 打开后，服务器上玩家的所有发言将不会在控制台显示，但仍会记录在日志中  
  - `check_libraries: true`    
    #: 检查运行所需的库，如果不存在，将自动下载  
  - `support_nocmd: false`    
    #: 使用面板服务器的部分用户需要启用此设置  
  - `disable_mods_blacklist: false`    
    #: 关闭模组黑名单检测，大多数是不兼容的或者是已经在 Mohist 内部实现的模组  
  - `disable_plugins_blacklist: false`    
    #: 关闭插件黑名单检测，大多数是不兼容的或者是已经在 Mohist 内部实现的插件  
  - `check_update_auto_download: false`    
    #: 检测到新版本时自动下载  
  - `realtimeticking: false`    
    #: 实时游戏运行(而不是使用游戏刻)，这个功能来自于 SpongeForge  
  - `watchdog_mohist: false`    
    #: Mohist 提供的看门狗  
  - `watchdog_spigot: true`    
    #: Spigot 提供的看门狗  
  - `showlogo: true`    
    #: 运行 Mohist 时会看到的字符LOGO  
