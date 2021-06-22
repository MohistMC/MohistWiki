## Mohist Build
---

> **Before starting, be sure you follow the [setup tutorial](./setup.md).**

### Steps
* Build Mohist
  * 1.12.2:
    * Build with Linux:  
      `bash gradlew setup installerJar`
    * Build with Windows:  
      `gradlew.bat setup installerJar`
  * 1.16.5:
    * Build with Linux:  
      `bash gradlew setup mohistJar`
    * Build with Windows:  
      `gradlew.bat setup mohistJar`

The Mohist server jar file is **located at .\projects\mohist\build\libs\mohist-xxxxx-server.jar**

This is the **jar file** that you should run.