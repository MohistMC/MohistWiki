## Velocity Support (1.20.1)
---

### How to use Velocity with Mohist ?

* GeyserMC can't work with Mohist if client side mods are used, since Minecraft Windows 10 edition can't use forge and mods.

-> __mohist-config/mohist.yml__
```
velocity:
  enabled: true
```
-> __server.properties__
```
online-mode=false //if you still want a premium only server you can set it inside of the waterfall's config file later
```
If you are trying to setup a proxy in local network you also need to change the "server-port" value in __server.properties__ -> set "server-port=25566" for example
(If you have more than one server, *you should have more than one server if you are running a proxy*, don't set the same value here for every servers.)

* Now, create a new folder for your Velocity proxy, and launch it using this java command:

```
java -jar <velocity jar name>.jar
```
* Then after the proxy is fully started, type "**end**" in the console to close your proxy.

* Now you need to change the __velocity.toml__ inside of your Velocity folder:

-> __velocity.toml__  
```
It is recommended to read the official documentation of velocity: https://docs.papermc.io/velocity/player-information-forwarding#configuring-modern-forwarding-for-paper
```

* Now you can start your proxy and all your Mohist servers!


## Velocity Support (1.20.2+)
---

### How to use Velocity with Mohist ?

* GeyserMC can't work with Mohist if client side mods are used, since Minecraft Windows 10 edition can't use forge and mods.

-> __mohist-config/mohist.yml__
```
velocity:
  enabled: true
```
-> __server.properties__
```
online-mode=false //if you still want a premium only server you can set it inside of the waterfall's config file later
```
If you are trying to setup a proxy in local network you also need to change the "server-port" value in __server.properties__ -> set "server-port=25566" for example
(If you have more than one server, *you should have more than one server if you are running a proxy*, don't set the same value here for every servers.)

* Now, create a new folder for your Velocity proxy, and launch it using this java command:

```
java -jar <velocity jar name>.jar
```
* Then after the proxy is fully started, type "**end**" in the console to close your proxy.

* Now you need to change the __velocity.toml__ inside of your Velocity folder:

-> __velocity.toml__  
```
player-info-forwarding-mode = "modern"
It is recommended to read the official documentation of velocity: https://docs.papermc.io/velocity/player-information-forwarding#configuring-modern-forwarding-for-paper
```

* Now you can start your proxy and all your Mohist servers!
