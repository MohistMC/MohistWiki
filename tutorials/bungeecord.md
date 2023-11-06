## Bungeecord Support
---

### How to use Bungeecord with Mohist ?

⚠️ **Disclaimer : You need to use Lightfall for 1.13+ forge servers, but remember that Lightfall is still in BETA and will likely not work with every mod.**

Recommended proxy softwares for Mohist:

- [Waterfall](https://papermc.io/downloads#Waterfall) (for Mohist 1.12.2)
- [Lightfall](https://github.com/ArclightPowered/lightfall) (for Mohist 1.16.5+)

* GeyserMC can't work with Mohist if client side mods are used, since Minecraft Windows 10 edition can't use forge and mods.

How to use **Waterfall** and **Lightfall**:

* In your Mohist server folder, after you have already ran it at least once, change these configs:

-> __spigot.yml__
```
bungeecord: true
```
-> __server.properties__
```
online-mode=false //if you still want a premium only server you can set it inside of the waterfall's config file later
```
If you are trying to setup a proxy in local network you also need to change the "server-port" value in __server.properties__ -> set "server-port=25566" for example 
(If you have more than one server, *you should have more than one server if you are running a proxy*, don't set the same value here for every servers.)

* Now, create a new folder for your Waterfall proxy, and launch it using this java command:

```
java -jar <waterfall jar name>.jar
```
* Then after the proxy is fully started, type "**end**" in the console to close your proxy.

* Now you need to change the __config.yml__ inside of your Waterfall folder:

-> __config.yml__
```
query_port: 25565 //keep the port of your hosting service if you are not in local
ip_forward: true
online_mode: true //or false if you want to enable cracked client
forge_support: true
```
```
servers:
  lobby:
    motd: '&1My Mohist server - Lobby'
    address: localhost:25566 //use the port of your "lobby" server
    restricted: false
```

⚠️ **FOR 1.16.5+ USERS:** Players need to download [Lightfall-client](https://github.com/ArclightPowered/lightfall-client/releases) to be able to join if your server require client side mods. You can also see the [source code](https://github.com/ArclightPowered/lightfall-client) of the lightfall client.

* Now you can start your proxy and all your Mohist servers!
