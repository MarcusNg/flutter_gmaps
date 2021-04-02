# Flutter Google Maps Tutorial

[YouTube Video](https://youtu.be/Zz5hMvgiWmY)

## Setup

- Get an API Key at [https://cloud.google.com/maps-platform/](https://cloud.google.com/maps-platform/)

- Enable Maps SDK for Android, Maps SDK for iOS, and Directions API.

- Add your API Key to the specified files

`android/app/src/main/AndroidManifest.xml`

```xml
<manifest ...
  <application ...
    <meta-data android:name="com.google.android.geo.API_KEY"
               android:value="YOUR KEY HERE"/>
```

`ios/Runner/AppDelegate.swift`

```swift
import UIKit
import Flutter
import GoogleMaps

@UIApplicationMain
@objc class AppDelegate: FlutterAppDelegate {
  override func application(
    _ application: UIApplication,
    didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
  ) -> Bool {
    GMSServices.provideAPIKey("YOUR KEY HERE")
    GeneratedPluginRegistrant.register(with: self)
    return super.application(application, didFinishLaunchingWithOptions: launchOptions)
  }
}
```

`lib/.env.dart`

```
const String googleAPIKey = 'YOUR KEY HERE';
```
