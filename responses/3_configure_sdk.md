# TomTom Lab: Maps SDK for Android

## ⌨️ Activity: install all required dependencies please proceed following steps:

### Choose Maps SDK modules for your app
Either independently include modules for Maps, Search and/or Routing or
all of them at once. You can do so by adding Maps SDK modules to
AndroidManifest.xml and build.gradle.

- MAP - [Getting started](https://developer.tomtom.com/maps-android-sdk/map-initialization)
- TRAFFIC - [Getting started](https://developer.tomtom.com/maps-sdk-android/getting-started)
- SEARCH - [Getting started](https://developer.tomtom.com/maps-android-sdk/getting-started)
- ROUTING - [Getting started](https://developer.tomtom.com/maps-android-sdk/getting-started-2)
- GEOFENCING - [Getting started](https://developer.tomtom.com/maps-sdk-android/getting-started-0)

### Configuration for all Maps SDK modules

To include all Maps SDK modules in your app, modify AndroidManifest.xml
and build.gradle  

#### Modify AndroidManifest.xml

Add service keys, taken from http://developer.tomtom.com, inside <application> tag.

```
<meta-data android:name="OnlineMaps.Key" android:value="undefined" />
<meta-data android:name="OnlineTraffic.Key" android:value="undefined" />
<meta-data android:name="OnlineSearch.Key" android:value="undefined" />
<meta-data android:name="OnlineRouting.Key" android:value="undefined" />
<meta-data android:name="GeofencingApi.Key" android:value="undefined" />
```

#### Modify build.gradle (app/build.gradle)

```
//library required to display map
implementation("com.tomtom.online:sdk-maps:2.4126")

//library required for search
implementation("com.tomtom.online:sdk-search:2.4126")

//library required for routing
implementation("com.tomtom.online:sdk-routing:2.4126")

//library required for traffic
implementation("com.tomtom.online:sdk-traffic:2.4126")

//library required for geofencing
implementation("com.tomtom.online:sdk-geofencing:2.4126")

//extencion library for map custom style and ui support
implementation("com.tomtom.online:sdk-maps-ui-extensions:2.4126")

//extencion library for rx-java2
implementation("com.tomtom.online:sdk-maps-rx-extensions:2.4126")

//extencion library for kotlin support
implementation("com.tomtom.online:sdk-maps-ktx-extensions:2.4126")

//extencion library for displaying static map
implementation("com.tomtom.online:sdk-maps-static-image:2.4126")

//extencion library for driving features
implementation("com.tomtom.online:sdk-maps-driving-extensions:2.4126")
```

#### Enable Java 8 Support in build.gradle (app/build.gradle)

```
android {
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}
```

#### Add MultiDex support if required, as described here

### Maps SDK Examples app

- Download and build the Maps SDK Examples app to see key features of the Maps SDK.
- Modify the source code to learn more about the SDK.
- Speed up development by using the source code in your own app.

Maps SDK Examples are hosted on github:
https://github.com/tomtom-international/maps-sdk-for-android-examples.

Clone repository by command:

```
git clone https://github.com/tomtom-international/maps-sdk-for-android-examples.git
```

This Maps SDK Examples app is provided by TomTom and subject to TomToms privacy policy at
https://tomtom.com/privacy

Developers using TomTom SDKs and APIs in their apps similarly bear responsibility to adhere to applicable privacy laws.

These Maps SDK Examples are provided as-is and shall be used internally, and for evaluation purposes only. Any other use is strictly prohibited.
