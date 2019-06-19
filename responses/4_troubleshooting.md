# TomTom Lab: Maps SDK for Android - Troubleshooting

Here you can find a list of possible issues and tips how to solve them:

## FindBugs JSF305 conflict:

Enforce Gradle to compile the fixed FindBugs version for all dependencies.
Add the following lines to your app’s build.gradle:

```
android {
    configurations.all {
        resolutionStrategy.force 'com.google.code.findbugs:jsr305:3.0.2'
    }
}
```

## MultiDex issues

MultiDex issues should be solved using [Google instructions](https://developer.android.com/studio/build/multidex.html).
However, find the most popular solutions below.

Configure your app for MultiDex. Add the following lines to your app’s build.gradle:

```
android {
    defaultConfig {
        multiDexEnabled true
    }
}
```

Add MultiDex support in your app’s build.gradle when minSdkVersion is set to 20 or lower:

```
dependencies {
    api 'com.android.support:multidex:1.0.1'
}
```

Increase java max heap size for dex support if required. Add the following lines to your app’s build.gradle:

```
android {
    dexOptions {
        javaMaxHeapSize "4g"
    }
}
```
