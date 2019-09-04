# TomTom Lab: Maps SDK for Android

Welcome to the TomTom Lab.

## Online documentation

All information about TomTom Maps SDK for Android can be found in
https://developer.tomtom.com/maps-sdk-android


## ⌨️ Activity: Get the pre-requisites in place:

Android Studio IDE installed (Android Studio)

Set up the application minimum API level to Android 4.4 "Jelly Bean" (API Level 16) or higher

Set up your project like this:
Open Android Studio IDE

## ⌨️ Activity: Create a new project or open an existing one

Add repositories to all projects to root/build.gradle:
```
allprojects {

   repositories {
      jcenter()
      google()
      maven {
         url 'https://maven.tomtom.com:8443/nexus/content/repositories/releases/'
      }
   }   
}
```
