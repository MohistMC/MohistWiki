# Common Problem

---
## Customize libraries:
Note: Libraries are mainly loaded by Class-Path  


### An example of using a custom libraries:

#### DefaultLibraries:  
\libraries\org\ow2\asm\asm-debug-all\5.2\asm-debug-all-5.2.jar  
Now we need to modify the version of asm-debug-all to 7.0

* First get asm-debug-all-7.0.jar  
* Change the file name to asm-debug-all-5.2 (because we need to be consistent with Class-Path)  
* Replace the old jar
* Modify the configuration in mohist.yml
    * Find the default `libraries_check.blacklist: aaaaa;bbbbbb`
    * Add `asm-debug-all-5.2` to the list: `libraries_check.blacklist: asm-debug-all-5.2;bbbbbb`
* You have completed all the steps and can run mohist

#### CustomLibraries:  
Add additional jars as libraries
* Put your jar file into`\libraries\customize_libraries`
* You have completed all the steps and can run mohist
