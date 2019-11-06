[![Build Status](https://api.cirrus-ci.com/github/mmcc007/default_flutter_app.svg)](https://cirrus-ci.com/github/mmcc007/default_flutter_app)

# default_flutter_app

This app was created using 
```
flutter create --with-driver-test --org com.mycompany.myflutterapp default_flutter_app
```
This created a testable flutter app that is runnable and testable. In practice, a separate deliverable flutter app and a testable flutter app is required. So the app was separated into a testable and a non-testable flutter app by this [commit](https://github.com/mmcc007/default_flutter_app/commit/1e72d1fea47999a26ccf90fdbc0ac9d4e6c0374c).

## Running and testing on a real device
To run the app as a non-testable app, make sure you have a device attached and run:
```
flutter run
or 
flutter --verbose run
```
To test the testable app, make sure you have a device attached and run:
```
flutter driver test_driver/main.dart
or 
flutter --verbose driver test_driver/main.dart
```
Note: for simplicity, testing in this context refers only to integration testing. It is still possible to run unit and widget tests on the 'non-testable' app. 

## iOS Deliverables
If an iOS device is attached, both flutter calls above create a `.app` file which is uploaded by flutter tooling to the device. The `.app` is signed using the developer certificate from the developer's Apple Developer Account. If the developer certificate is not present, it can be downloaded from Xcode by following the 'Automatic Signing' procedure.

Delivering the app to the app store or to another iOS device generally requires creating a `.ipa` and is beyond the scope of this document.