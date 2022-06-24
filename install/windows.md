## Windows installation

---
Requirements
---

Please read the [requirements page](install/requirements.md) before reading this page.

---
Download
---

You can download the latest version from our [Website](https://mohistmc.com/download) or our [Jenkins](https://ci.codemc.org/job/MohistMC/).

Install
---

### 1.19.X installation

The 1.19.X installation is different from others, because it comes with an installer.

When you downloaded the Mohist 1.19 jar file, place it in a folder, double click on it, select install server, then select the current folder path above Ok button, and click Ok.
The server is being installed.  

When it's done, you can run your server by opening a terminal and executing run.bat.

### Others

When you downloaded the jar file, place it in **an empty directory**.

Now launch it using the `java` command:     
_For users who knows how it works, you can skip the extra steps._

```bash
java -jar mohist-<mcversion>-<buildnumber>-server.jar
```

**You don't know how this works ?**    
Take the command above, replace `<mcversion>` by the version you downloaded (1.12.2, 1.16.5 or 1.7.10), and replace `<buildnumber>` by the build number.    

How to run this command ?     
Open file explorer to your server folder, and then press `shift` and `right click` button, and open with command prompt (CMD), and paste the command above.
