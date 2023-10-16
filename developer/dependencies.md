## Dependencies

---

It is recommended to use the official template for plugin development.  
https://github.com/MohistMC/MohistPlugin

### 1.12.2
```
 repositories {
    maven { url "https://maven.mohistmc.com/"}
    maven { url 'https://hub.spigotmc.org/nexus/content/groups/public/' }
    maven { url 'https://libraries.minecraft.net/' }
    maven { url 'https://maven.minecraftforge.net/' }
 }

dependencies {
    implementation 'com.mohistmc:mohistdev:0.1-SNAPSHOT'
}
```

### 1.16.5
```
 repositories {
    maven {url "https://maven.mohistmc.com/"}
 }

dependencies {
    implementation 'com.mohistmc:mohistdev:1.16.5'
}
```


### 1.20.1+ (1.20.1|1.20.2)
```
 repositories {
    maven {url "https://maven.mohistmc.com/"}
 }

dependencies {
    implementation 'com.mohistmc:mohistdev:<mc_version>'
}
```