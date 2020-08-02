# qrcode_reader

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.


Refer link:
1. QR code scanner: https://pub.dev/packages/qr_code_scanner
2. Flutter launcher icons: https://pub.dev/packages/flutter_launcher_icons

3. Build and release an Android app: https://flutter.dev/docs/deployment/android

To use qr code scanner:
1. Add qr_code_scanner: ^0.0.13 into pubspec.yaml.
2. Add <uses-permission android:name="android.permission.CAMERA" /> into AndroidManifest.xml
3. Change minSdkVersion to 24 into build.gradle

Add flutter launcher icons:
1. Add following code into pubspec.yaml.

    flutter_launcher_icons: ^0.7.5

    flutter_icons:
    android: true
    ios: true
    image_path: "assets/icon/QR Code Reader(Tested) Icon.pn

2. Run command below.

    flutter pub get
    flutter pub run flutter_launcher_icons:main

To Signing the app:
1. Create a keystore (if existing, skip this step)
- keytool -genkey -v -keystore ~/key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias key
*** Keep this file private,  do not check it into public source control.
***  keytool might not be in your path. It is part of the Java JDK, which is installed as part of Android Studio. For the concrete path, run flutter doctor -v and see the path printed after ‘Java binary at:’, and then use that fully qualified path replacing java with keytool.
*** Keytool prompts you to provide passwords for the keystore, provide the Distinguished Name fields and then the password for your key. It then generates the keystore as a file called my-release-key.keystore in the directory you're in. The keystore and key are protected by the passwords you entered. The keystore contains a single key, valid for 10000 days. The alias is a name that you — will use later, to refer to this keystore when signing your application.


#   Q R - C o d e - S c a n n e r  
 