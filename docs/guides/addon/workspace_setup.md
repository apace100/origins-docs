---
title: Workspace Setup
date: 2021-07-17
---
# Setting up the workspace

So, you want to create an Origins add-on? Nice.

Before you start, let me just say that I assume you have worked with Fabric before in some capacity and have at least general programming knowledge. I'm not going to explain every necessary Java concept here, but focus on what Origins does and how you can add your own features.

To begin developing an add-on, you need to set up your workspace. The first step is setting it up like any other Fabric modding workspace, outlined here: [Fabric Wiki (Setup)](https://fabricmc.net/wiki/tutorial:setup)

Once that's done and you have a mod that runs (even though it doesn't do anything yet), you should be able to add Origins to your gradle build script, so that the workspace automatically downloads the mod. In your `build.gradle` file, add the following Maven repositories if you don't have them already:
```
repositories {
	maven {
		name = "Ladysnake Libs"
		url = 'https://ladysnake.jfrog.io/artifactory/mods'
	}
	maven {
		url = 'https://maven.cafeteria.dev'
		content {
			includeGroup 'net.adriantodt.fabricmc'
		}
	}
	maven {
		url "https://maven.jamieswhiteshirt.com/libs-release"
		content {
			includeGroup "com.jamieswhiteshirt"
		}
	}
	maven {
		url "https://jitpack.io"
	}
	maven {
		url "https://maven.shedaniel.me/"
	}
	maven {
		url "https://api.modrinth.com/maven"
	}
}
```
Note: this block goes into the file directly (at the top level); do **not** add JitPack to the `publishing { repositories { ... } }` you see at the bottom of your `build.gradle`.

Once you did this, you also need to add this line to your `dependencies` block:
```
modImplementation "com.github.apace100:origins-fabric:${project.origins_version}"
```

The `${project.origins_version}` is a variable which will be taken from `gradle.properties`. It's just a neat way to set things up, so you don't have to mess with your `build.gradle` every time you want to update a mod. Theoretically, you could just add the version directly in the `build.gradle`. However, to define the variable, open up your `gradle.properties` file and add a line which looks like this:

```
origins_version=v1.0.0
```

Replace `v1.0.0` with the version of Origins you want to use. Usually, using the latest version is recommended. You can find the version numbers here: [GitHub Releases](https://github.com/apace100/origins-fabric/releases)

Alternatively, you can specify the branch you want to use and append `-SNAPSHOT` to it, to get the latest (unreleased) version from a branch. One example would be `origins_version=1.17-SNAPSHOT` to get the latest commits for the 1.17 version of Origins! Have a look at [Origins on JitPack](https://jitpack.io/#apace100/origins-fabric) to see the available versions and view their build status.

**Note:** JitPack builds the projects you request on demand. That means if you're the first to request a specific Origins version, it might take a while for JitPack to build it, and it's likely that it'll fail the first time due to a timeout. Just try again, it usually works on the second or third try. If it doesn't, check JitPack for errors.

That's it! If you refresh gradle, Origins should be included in your project. Hooray!
Test it by running your project now - you should be able to choose an origin when you join a world now, because Origins is now included in your development environment.
