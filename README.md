# Golan IPTV Pro

[Practical guide and cost/PC FAQ](GUIDE.md)

[العربية](README.ar.md)


Flutter IPTV player for Android and Android TV. Current version: **4.6.0+9**; the supplied ARM64 split APK reports version code **2009**. Application ID: `com.golan.iptv.golan_iptv_pro`.

## Download and install

Get the unchanged existing **ARM64 Debug APK** and complete source ZIP from [Releases](https://github.com/GOLAN2CODE/golan-iptv-pro/releases). Extract the source ZIP before building. The supplied APK requires Android 7 / API 24 or later and an ARM64 device. It is a development build. A matching certificate is required to update an installed copy.

```powershell
adb install -r Golan-IPTV-Pro-arm64-debug.apk
```

## Features

- M3U/Plus, direct HLS/TS, Xtream Codes, Stalker MAC and activation-code connection options, with stored server roles and matching-channel fallback.
- Persistent player across browsing, fullscreen, channel drawer and in-app mini dock; recent channels, quick zapping and Android foreground background audio.
- Arabic/English UI, parental controls and metadata filtering, channel refresh and verification, playback cache profiles and network diagnostics.
- Credentials stored using Flutter secure storage and Android Keystore; masks in the management UI, with no plaintext fallback when secure storage fails.

## Demo subscriptions and service limits

No real paid subscription or activation backend is bundled. With the activation endpoint blank, `111222` / `GOLAN-VIP` selects a **simulated VIP lineup**; `999000` / `GOOGLE-TEST` selects isolated reviewer test sources. These codes do not grant a paid subscription. Configure a compatible HTTPS backend according to `Documentation/Device-Activation-API.md` or enter your own authorized provider credentials. Public playlists and upstream streams can change or stop working. Availability is not guaranteed, and this package does not grant rights to rebroadcast or access restricted content.

The mini dock is inside the app. Rewind depends on available media/cache range. The latency indicator measures catalog HTTP response time, not a guaranteed streaming ping. Filtering uses metadata and cannot guarantee every item is classified correctly. No independent security audit is claimed.

## Build from the source ZIP

Install a Flutter SDK providing Dart `^3.13.5`, JDK 21 and the Android SDK/NDK versions selected by that Flutter toolchain and the checked-in Gradle files. Start in the extracted root containing `pubspec.yaml`; restoration requires the network.

```powershell
flutter pub get
flutter build apk --debug --target-platform android-arm64 --split-per-abi
```

`scripts/flutter.ps1` can use Flutter on PATH or your private local SDK configuration. Release builds require your own `GOLAN_KEYSTORE`, `GOLAN_STORE_PASSWORD`, `GOLAN_KEY_ALIAS` and `GOLAN_KEY_PASSWORD` environment values. Signing keys and local workstation configuration are excluded. Existing tests remain in `test/`; no new app build or functional tests were run for this publication package.

`test/fixtures/localhost.crt` and `localhost.key` are deliberately public, self-signed **test-only** localhost TLS fixtures used by existing tests. They must never be used for a production service. See `THIRD_PARTY.md`, `THIRD_PARTY_NOTICES.txt`, `LICENSE_STATUS.md` and `PRIVACY.md`. No new license is assigned to the owner's application code.
