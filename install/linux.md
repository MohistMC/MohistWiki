## Linux installation

---
Requirements
---

Please read the [requirements page](install/requirements.md) before reading this page.

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
* 1.18.X:
    ```bash
    wget https://mohistmc.com/api/1.18-testing/latest/download
    ```
    
---
Install
---

### 1.19 Installation

When you downloaded the jar file, place it in **an empty directory**.

The 1.19.X installation is different from others, because it comes with an installer.       

Now run the installer using the `java` command:
```bash
java -jar mohist-<mcversion>-<buildnumber>-installer.jar --installServer
```

When the installation is finished, you can run your server using this command:
```bash
./run.sh
```

### Others
When you downloaded the jar file, place it in **an empty directory**.

Now launch it using the `java` command:

```bash
java -jar mohist-<mcversion>-<buildnumber>-server.jar
```
