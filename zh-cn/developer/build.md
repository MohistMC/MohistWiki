## Mohist 构建
---

> **开始之前，请确保你已完成了[配置 Mohist 开发环境](developer/setup.md)。**

### 构建步骤
* **1.7.10**
  * 在 Linux 上构建：
    `bash gradlew setupCauldron launch4j`
  * 在 Windows 上构建：
    `gradlew.bat setupCauldron launch4j`
* **1.12.2**
  * 在 Linux 上构建：
    `bash gradlew setup installerJar`
  * 在 Windows 上构建：
    `gradlew.bat setup installerJar`
* **1.16.5 - 1.20.4**
  * 在 Linux 上构建：
    `bash gradlew setup mohistJar`
  * 在 Windows 上构建：
    `gradlew.bat setup mohistJar`

Mohist server ja r文件**位于** `./projects/mohist/build/libs/mohist-xxxxx-server.jar`

这是你应该运行的**jar文件**。
