# Adding Tardis Refined to your Project

In order to add Tardis Refined to your project and begin developing, you will need to create
a [architectury](https://github.com/architectury/architectury-templates/releases) project

You will need to ensure that your architectury project has the correct Minecraft Version setup in order to begin
developing. Throughout this guide, we assume you have at least some experience with writing in Java, and creating
Minecraft Mods.

## Repository Management

In order to source Tardis Refined, we will be using
the [Modrinth maven](https://support.modrinth.com/en/articles/8801191-modrinth-maven). This helps to assist in
developing against released versions in order to maintain addon mod compatibility. We will also add some other mavens in order to source required dependencies for the project

Within your project, locate the ``build.gradle`` found at the route of your project and navigate to the allProjects
block

```Groovy
allprojects {
    apply plugin: "java"
    apply plugin: "architectury-plugin"
    apply plugin: "maven-publish"
    ...
}
```

Within this block, find the repositories sub-block, this may already have content in it

```Groovy
repositories {

}
```

Once located, add the following Maven Repositories

```Groovy
repositories {
    // Modrinth Maven
    maven {
     url = "https://api.modrinth.com/maven" 
    }
    
    // Ladysnake Maven, required for CardinalComponents
    maven {
       name = 'Ladysnake Mods'
       url = 'https://maven.ladysnake.org/releases'
    }
    
    // Fuzzs Mod Resources, required for ForgeConfigAPIPort
     maven {
        name = "Fuzs Mod Resources"
        url = "https://raw.githubusercontent.com/Fuzss/modresources/main/maven/"
     }
}
```

## Preparing gradle.properties
Locate the gradle.properties within the root of your project, and open it
![](gradle_properties.png)

Within this file, add the following entries:
```Groovy
forge_config_api_port_version=<VERSION>
tardis_refined_version=<VERSION>
tardis_refined_version_forge=<VERSION>
cardinalcomponents_version=<VERSION>
```

You will want to update these values based on the Minecraft Version you are using, you can potentially use the [Tardis Refined Github Repository](https://github.com/WhoCraft/TardisRefined) to find relevant values


## Adding to Common & Fabric Modules

In order to reference and code against the mod, we must mainly add it to the common and fabric modules, enter the common module and
locate the ``build.gradle``

| ![Common Build Gradle](common_build_gradle.png) | ![Fabric Build Gradle](fabric_build_gradle.png) | ![Forge Build Gradle](forge_build_gradle.png) |
|:--:|:--:|:--:|
| Common Build Gradle | Fabric Build Gradle | Forge Build Gradle |



Once you have entered the file, locate the dependencies block which should look something like:
```Groovy
dependencies {
    modImplementation "net.fabricmc:fabric-loader:${rootProject.fabric_loader_version}"
}
```

Update the dependencies block to look like this

```Groovy
dependencies {
    modImplementation "net.fabricmc:fabric-loader:${rootProject.fabric_loader_version}"
   
    // Cardinal Components
    modImplementation "dev.onyxstudios.cardinal-components-api:cardinal-components-base:${rootProject.cardinalcomponents_version}"
    modImplementation "dev.onyxstudios.cardinal-components-api:cardinal-components-world:${rootProject.cardinalcomponents_version}"
    
    // Tardis Refined
    modImplementation "maven.modrinth:tardis-refined:${tardis_refined_version}"
    
    // Forge Config API Port
    modImplementation "fuzs.forgeconfigapiport:forgeconfigapiport-fabric:${rootProject.forge_config_api_port_version}"
}
```

## Adding to Forge Module
Following from earlier, we navigate to the Forge ``build.gradle`` which has a different yet similar approach, where we add the following

```Groovy
dependencies {
  // Tardis Refined
    modImplementation "maven.modrinth:tardis-refined:${tardis_refined_version_forge}"
}
```