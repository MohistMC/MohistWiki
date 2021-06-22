## Linux installation

---
Requirements
---

Mohist **1.12.2** requires **[Java 8](https://adoptopenjdk.net/?variant=openjdk8&jvmVariant=hotspot)**.

Mohist **1.16.5** requires **[Java 11](https://adoptopenjdk.net/?variant=openjdk11&jvmVariant=hotspot)**.

---
Download
---

You can download the latest version from our [Website](https://mohistmc.com/download) or our [Jenkins](https://ci.codemc.org/job/MohistMC/).

You can also use **wget** command if you want. 

Example : 
* 1.12.2:
    ```bash
    wget https://mohistmc.com/api/1.12.2/latest/download
    ```
* 1.16.5:
    ```bash
    wget https://mohistmc.com/api/1.16.5/latest/download
    ```
    
---
Install
---

When you downloaded the jar file, place it in **an empty directory**.

Now launch it using the `java` command:

```bash
java -jar mohist-<mcversion>-<buildnumber>-server.jar
```
