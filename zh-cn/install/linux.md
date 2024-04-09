## Linux安装

---
需求
---

在阅读此页之前，请阅读 [需求清单](install/requirements.md)

---
下载
---

你可以从我们的 [官方下载渠道](https://mohistmc.com/download) 或者 [Jenkins](https://ci.codemc.org/job/MohistMC/) 下载最新构建。

你也可以手动使用**wget**来下载。

示例 : 

```bash
wget https://mohistmc.com/api/<mc-version>/latest/download
```
---
安装
---

当安装完成后，在bash中执行以下命令来启动:
```bash
./run.sh
```

### 杂项
当你下载完jar文件之后，请将它放置在 **空目录**.

现在使用`java`来启动它：

```bash
java -jar mohist-<mcversion>-<buildnumber>-server.jar
```
