# Golan IPTV Pro — practical guide

[العربية](GUIDE.ar.md) · [Overview and source build](README.md) · [Downloads](https://github.com/GOLAN2CODE/golan-iptv-pro/releases)

## Install and understand the package

The current source version is 4.6.0+9; the supplied split APK reports build 2009. It is an ARM64 Debug build requiring Android 7 / API 24 or later. Install it on a compatible phone or Android TV device; matching signing certificates are required for an in-place update. The package is a player, not a purchased television subscription or a guarantee that any channel remains available.

## Add a source you are entitled to use

Supported inputs include a full M3U/Plus playlist URL, direct HLS/TS media address, Xtream Codes server address with username/password, Stalker portal with MAC details, or an activation code with a compatible HTTPS endpoint. Enter the fields for your provider's protocol rather than treating these connection types as interchangeable. Subscription/account details shown by the app come from the provider response.

For local demonstration, leave the activation endpoint blank. The documented VIP demo and reviewer codes select simulated lineups/test streams; they do not buy access or connect to a bundled paid backend. To activate a real account, a compatible external service must be configured. Public source addresses and channels can disappear, change restrictions or stop responding.

Assign a primary and backup role when managing multiple sources. Fallback looks for matching channel identity; an unrelated station is not a substitute. Credentials are masked in management screens and stored through secure storage. If secure storage fails, settings can remain session-only with a warning. Keep your provider details safely elsewhere rather than relying on reinstalling the app to recover them.

## Browse, watch and diagnose

Choose a channel from the available list and use the player while browsing, opening the channel drawer or switching to fullscreen. The mini dock stays inside the app. Previous/next controls and horizontal swipes move through the filtered channel list; recent channels help return to successfully started stations. Android foreground playback supports background audio, subject to the system's restrictions and permissions.

Channel refresh gathers public sources, filters metadata, checks playable media and ranks results. It does not renew a paid subscription. Cache profiles change buffering behavior; rewind works only within the available media/cache range. Network diagnostics help distinguish a slow response or failed source from a player issue. The latency badge is an HTTP measurement, not guaranteed end-to-end video latency. Parental/metadata filtering is useful but cannot classify every stream correctly.

## Cost and PC FAQ

A focused source review found no personal billed developer API key, AI-credit usage or payment integration. If you enter a paid subscription, its charges and connection limits belong to your agreement with that provider. Streaming uses internet data and can consume significant mobile allowance; background playback also uses data.

**Your PC and Codex do not need to stay running after installation.** Playback and the loopback HLS relay run on the Android device; loopback is not a server on your computer. Streaming still needs the selected external media service and network. See [data handling](PRIVACY.md), [third-party information](THIRD_PARTY.md) and [license status](LICENSE_STATUS.md); this package does not grant broadcast or restricted-content rights.
