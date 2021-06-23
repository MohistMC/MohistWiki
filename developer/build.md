## Mohist Build
---

> **Before starting, be sure you followed the [setup tutorial](./setup.md).**

### Steps
* Build Mohist
  ### Building
  * **1.7.10**:
    * Build with Linux:  
      `git clone -b 1.7.10 https://github.com/MohistMC/Mohist.git`  
      `git submodule update --init --recursive`  
      `bash gradlew setupCauldron launch4j`
    * Build with Windows:  
      `git clone -b 1.7.10 https://github.com/MohistMC/Mohist.git`  
      `git submodule update --init --recursive`  
      `gradlew.bat setupCauldron launch4j`
  * **1.12.2**:
    * Build with Linux:  
      `bash gradlew setup installerJar`
    * Build with Windows:  
      `gradlew.bat setup installerJar`
  * **1.16.5**:
    * Build with Linux:  
      `bash gradlew setup mohistJar`
    * Build with Windows:  
      `gradlew.bat setup mohistJar`

The Mohist server jar file is **located at** `./projects/mohist/build/libs/mohist-xxxxx-server.jar`

This is the **jar file** that you should run.