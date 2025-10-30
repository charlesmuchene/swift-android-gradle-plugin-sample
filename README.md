# Swift Android Gradle Plugin Sample

<img src="media/app.gif" alt="Demo" width="480">

This sample project demonstrates the use of the [Swift Android Gradle Plugin](https://github.com/charlesmuchene/swift-android-gradle-plugin) to include Android application logic written in _Swift_ code.

## Applying the plugin

> Plugin is not yet published to any repository -- using `includedBuild` workaround.

```kotlin
// build.gradle.kts
plugins {
   // android app/lib plugin must be applied first

   id("com.charlesmuchene.swift-android-gradle-plugin") version "0.1.0-alpha"
}

// settings.gradle.kts
pluginManagement {
   repositories {
      // ...
   }

   // NOTE: Plugin is not yet published to any repository
   // Clone and add plugin as an included build
   includeBuild("../swift-android-gradle-plugin")
}
```

## Project Structure

```
app
├── build.gradle.kts
└── src
    └── main
        ├── AndroidManifest.xml
        ├── java
        │   └── com
        │       └── charlesmuchene
        │           └── sample
        │               ├── MainActivity.kt
        │               └── Compose UI
        ├── res
        │   ├── drawable
        │   └── values
        ├── swift
        │   ├── Package.swift
        │   └── Sources
        │       └── lib.swift
        └── build.gradle.kts
            └── swift-android-gradle-plugin
```
