## checklist for updating to newer forge version

Just a simple checklist for myself, when I want to update this mod to a newer version.

### 0. Have a backup!

### 1. run script to apply mappings to the code

(replace the mappings id (YYYYMMDD-1.XX.X), see 2. for where to find it)
```
./gradlew -PUPDATE_MAPPINGS="20201028-1.16.3" -PUPDATE_MAPPINGS_CHANNEL="snapshot" updateMappings
```

### 2. update build.gradle

**update mappings channel**

`29 | mappings channel: 'snapshot', version: '...'`
 
checkout the forge discord server https://discord.gg/UvedJ9m
 
newest mapping is probably pinned in the modder-support-... channel
 
mapping can be a version lower than the minecraft version you are developing for
 
forge devs are currently developing a new system for the mappings, so stuff might change

**update forge version**

`94 | minecraft 'net.minecraftforge:forge:1.16.4-35.1.4'`

find newest (stable) version on https://files.minecraftforge.net/

### 3. change the minecraft version in mods.toml

### 4. Reload gradle changes

### 5. Run the genIntellijRuns gradle task

### 6. File > Reload all from disk

### 7. Increase version

Increase version id in build.gradle

### 8. Run tasks

Run 'build', 'runClient' and 'publish' tasks and make sure everything works.

Try out the published jar in the mod launcher

### 9. Change version in README 

Update the version in the "Installing this mod with the Forge Mod Launcher" section