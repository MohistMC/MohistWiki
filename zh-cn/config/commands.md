## Mohist 命令
---

> 此处列出了 Mohist 的所有命令。

**重要**：此命令列表会因您的 Mohist 版本（如1.12.2或1.16.5）而有所不同。这里的某个命令可能在某个版本上不可用，但将很快实现。

---

* `/mohist [mods|playermods|printthreadcost|lang|item|reload|give]` 
    权限节点：*mohist.command.mohist*

    参数 `mods`：列出服务器模组列表 
    参数 `playermods`：列出一个玩家的模组列表（需要第二个参数）
    参数 `printthreadcost`：打印 Mohist 线程消耗。
    参数 `lang`：显示当前 Mohist 语言。
    参数 `item`：显示方块/物品信息（执行此命令时需要手持方块/物品）
    参数 `reload`：重新加载 Mohist 配置文件。
    参数 `give`：一个支持模组方块/物品的 give 命令。

---

* `/backupworld <worldname>`
    权限节点：*mohist.command.backupworld*

    这个命令可以让你在服务器运行时创建一个世界的zip文件备份，且不会冻结服务器。

---

* `/downloadfile <filename> <path> <url>` 
    权限节点：*mohist.command.downloadfile*

    这个命令允许你从互联网下载文件。你需要在`mohist.yml`中将`downloadfile_command_enabled`设置为`true`以启用此命令。
    > 免责声明：不要允许不明人士使用此命令！

---

* `/dump <file|web> [potions|enchants|cbcmds|modscmds|entitytypes|biomes|pattern|worldgen|worldtype|bukkit_material|vanilla_material]` 
    权限节点：*mohist.command.dump*

    这个命令可以将您想要的信息以可用的参数形式转储出来。转储结果可以通过两种方式提供：网页（hastebin）或文件。

---

* `/entity [reload|dump-existing]`
    权限节点：*mohist.command.entity*

    参数 `reload`：重新加载 `entities.yml` 配置文件。
    参数 `dump-existing`：用已有的实体更新 `entities.yml`。

---

* `/getmodlist`
    权限节点：*mohist.command.getmodlist* 

    这个命令会将您的模组列表及所有详细信息粘贴到 hastebin 页面上。完成后会返回给您网址。

---

* `/getpluginlist`
    权限节点：*mohist.command.getpluginlist*

    这个命令会将您的插件列表及所有详细信息粘贴到hastebin页面上。完成后会返回给您网址。

---

* `/plugin [load|unload|reload] [name]`
    权限节点：*mohist.command.plugin*

    参数 `load`：加载插件
    参数 `unload`：卸载插件
    参数 `reload`：重新加载插件
    参数 `name`：插件名称

    这个命令允许您加载、卸载或重新加载特定插件。

---

* `/whitelistmods [enable|disable|update]`
    权限节点：*mohist.command.whitelistmods*

    参数 `enable`：启用模组白名单
    参数 `disable`：禁用模组白名单
    参数 `update`：在 mohist.yml 中自动更新服务器模组列表

    这个命令是 `mohist.yml` 提供的一个功能，它允许你在服务器上只允许特定的模组。指定 `enable` 参数时，列表将自动填充服务器模组列表。你可以在 `mohist.yml` 文件中手动编辑允许的模组列表。

---

* `/updatemohist`
    权限节点: *mohist.command.updatemohist*

    这个命令是 `mohist.yml` 提供的一个功能，它允许你在需要时在启动时更新 Mohist。执行这个命令后，它将启用或禁用更新程序下载。