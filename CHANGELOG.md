## 1.3.1

### Fixed
- iOS: Removed an invalid `flutter_wrapper` package reference from the SwiftPM target manifest that caused `unknown package 'flutter_wrapper' in dependencies of target 'vpn_detector'` build failures when SwiftPM integration was enabled. The target now declares its `Sources/vpn_detector` path explicitly, matching the first-party Flutter plugin pattern. Thanks to @AlexV525 (#12).

## 1.3.0

### Added
- Added Swift Package Manager (SwiftPM) support for iOS.

### Changed
- Migrated iOS source files to SwiftPM-compatible directory layout.
- Removed Objective-C bridge layer; plugin now registers directly via Swift.
- Widened `connectivity_plus` dependency to `>=6.1.4 <8.0.0` to support v7.x.
- Updated minimum Flutter SDK to 3.24.0.
- Updated minimum Dart SDK to 3.0.0.
- Synced podspec version to 1.3.0.

## 1.2.0

### Breaking Changes
- Changed `VpnDetector.isVpnActive()` return type from `Future<bool>` to `Future<VpnStatus>`, introducing the `VpnStatus` enum.

### Added
- Introduced `VpnStatus` enum with values `active` and `notActive`.
- Added `onVpnStatusChanged` stream for real-time VPN status updates.
- Added `VpnDetector.withDependencies(...)` constructor (annotated `@visibleForTesting`) for dependency injection and TDD.

## 1.1.1

### What's Changed

- Documentation dart api

## 1.1.0

### What's Changed

- **Android**: Updated to `compileSdk=35`, `minSdk=21`, `targetSdk=35`.
- **iOS**: Minimum deployment target set to `iOS 13.0`, Swift `5`.

## 1.0.1

### What's Changed

- Enhanced documentation in the README.md
- Upgraded dependencies to the latest versions
- Add more tests for `vpn_detector_method_channel_test.dart`

## 1.0.0

### What's Changed

- Detect VPN active connections on Android and IOS Platforms
