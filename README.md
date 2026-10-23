# TELYRA - Official Distribution and Releases

[![Release](https://img.shields.io/github/v/release/b4lol/telyra-releases?color=00f0ff&label=Latest%20Version)](https://github.com/b4lol/telyra-releases/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Android%20TV%20%7C%20Google%20TV%20%7C%20Mobile-blue)](https://github.com/b4lol/telyra-releases)
[![Telemetry](https://img.shields.io/badge/Telemetry-0%25%20%28Zero%20Tracking%29-brightgreen)](https://b4.lol/telyra/privacy/)
[![Security](https://img.shields.io/badge/Security-AndroidKeyStore%20AES--256--GCM-blueviolet)](https://b4.lol/telyra/)

TELYRA is an enterprise-grade cinematic IPTV and media client engineered exclusively for Android TV, Google TV, Fire OS, and Android Mobile devices. Built with modern Kotlin and optimized rendering pipelines, it achieves consistent 60 FPS compositor navigation, hardware deinterlacing, and fast channel switching within strict memory boundaries (<45MB JVM heap budget).

Official Website: [https://b4.lol/telyra/](https://b4.lol/telyra/)  
Privacy Policy: [https://b4.lol/telyra/privacy/](https://b4.lol/telyra/privacy/)

---

## Downloads (Latest Release: v1.1.0)

| Package | Target Form Factor | File Type | Size | SHA-256 Checksum |
| :--- | :--- | :--- | :--- | :--- |
| **[TELYRA Android TV](https://github.com/b4lol/telyra-releases/releases/download/v1.1.0/app-tv-release.apk)** | Android TV / Google TV / Fire TV | `.apk` | ~85.6 MB | `871e38bd00468fb6a71bfcc0a04fa38a5cfbc57e311e29ac1a34ff8cc40b0218` |
| **[TELYRA Mobile](https://github.com/b4lol/telyra-releases/releases/download/v1.1.0/app-mobile-release.apk)** | Android Phones & Tablets | `.apk` | ~178.9 MB | `2093f1ad37d42329734ee4068ebbb1d7757625f3d10b11521ad232a98b098f27` |

> Integrity Verification:  
> Verify downloaded binaries on Linux / macOS via:
> ```bash
> sha256sum app-tv-release.apk
> ```
> Or on Windows PowerShell:
> ```powershell
> Get-FileHash -Algorithm SHA256 app-tv-release.apk
> ```

---

## What's New in v1.1.0

- Stalker / MAG portal middleware integration (`/server/load.php` element-by-element streaming parser).
- Jellyfin media server provider support for movies and series libraries.
- Plex Media Server direct connection support.
- Stremio add-on protocol client for official HTTPS manifest specifications.
- Memory optimizations maintaining low-end Android TV stick stability.

---

## How to Install on Android TV / Google TV

### Method 1: Using "Downloader by AFTVnews" (Fastest)
1. Install **Downloader** by AFTVnews from Google Play Store on your TV.
2. Open Downloader and enter the direct APK link into the URL box:
   ```
   https://github.com/b4lol/telyra-releases/releases/download/v1.1.0/app-tv-release.apk
   ```
3. Select **Go** to download and install. When prompted, allow installing unknown apps for Downloader.

### Method 2: Via ADB (Command Line)
Connect your computer to your TV over Wi-Fi or USB:
```bash
adb connect <TV_IP_ADDRESS>:5555
adb install -r app-tv-release.apk
```

### Method 3: USB Flash Drive
1. Download `app-tv-release.apk` to a FAT32 or exFAT formatted USB drive.
2. Plug the USB drive into your Android TV box.
3. Open a TV File Manager (such as FX File Explorer) and select the APK to install.

---

## Security and Privacy Architecture

1. **Zero Telemetry and Zero Analytics:**  
   TELYRA contains no Google Firebase Analytics, no tracking SDKs, and no advertisement modules.
2. **Hardware-Backed Cryptography:**  
   Source credentials and tokens never leave your local device. They are sealed with AES-256-GCM via the hardware-backed `AndroidKeyStore` (Titan M, Knox, or ARM TrustZone).
3. **Optimized Playback Engine:**  
   Media3 ExoPlayer and LibVLC dual-engine architecture with adaptive buffer management, hardware-accelerated codec decoders, and low-latency bitstream detection.

---

## Bug Reports and Feature Requests

For issues with specific streams, codecs, or Android TV hardware models:  
Open a ticket on our **[Issue Tracker](https://github.com/b4lol/telyra-releases/issues)** with:
- Device Model (e.g. Nvidia Shield Pro, Chromecast with Google TV, Xiaomi TV Box S)
- Android OS version (Android 9 / 10 / 11 / 12 / 14)
- Playback engine used (Media3 ExoPlayer or LibVLC)
- Reproduction steps

---

## Legal Notice

TELYRA is a standalone media player client. It does not host, provide, or bundle any media content, playlists, or IPTV streams. Users are solely responsible for adding their own legitimate media sources.

*(C) 2026 TELYRA Team. All rights reserved.*
