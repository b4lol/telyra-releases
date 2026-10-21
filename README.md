# 📺 TELYRA — Official Distribution & Releases

[![Release](https://img.shields.io/github/v/release/b4lol/telyra-releases?color=00f0ff&label=Latest%20Version)](https://github.com/b4lol/telyra-releases/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Android%20TV%20%7C%20Google%20TV%20%7C%20Mobile-blue)](https://github.com/b4lol/telyra-releases)
[![Telemetry](https://img.shields.io/badge/Telemetry-0%25%20%28Zero%20Tracking%29-brightgreen)](https://b4.lol/telyra/privacy/)
[![Security](https://img.shields.io/badge/Security-AndroidKeyStore%20AES--256--GCM-blueviolet)](https://b4.lol/telyra/)

**TELYRA** is a next-generation cinematic IPTV and media client engineered exclusively for Android TV, Google TV, Fire OS, and Android Mobile devices. Built with pure Java 17 and native Android view hierarchy (zero-Compose runtime overhead), it achieves a rock-solid 60 FPS compositor lock, 0ms Amlogic hardware deinterlacing, and sub-second channel zapping.

Official Website & Interactive Telemetry: **[https://b4.lol/telyra/](https://b4.lol/telyra/)**  
Privacy Policy: **[https://b4.lol/telyra/privacy/](https://b4.lol/telyra/privacy/)**

---

## 🚀 Downloads (Latest Release: v1.0.0)

| Package | Target Form Factor | File Type | Size | SHA-256 Checksum |
| :--- | :--- | :--- | :--- | :--- |
| **[TELYRA Android TV](https://github.com/b4lol/telyra-releases/releases/download/v1.0.0/app-tv-release.apk)** | Android TV / Google TV / Fire TV | `.apk` | ~86 MB | `e5ef32fa5169ac6f1a351bc5503ec979867b03642e06d21e9b6b4461792d6174` |
| **[TELYRA Mobile](https://github.com/b4lol/telyra-releases/releases/download/v1.0.0/app-mobile-release.apk)** | Android Phones & Tablets | `.apk` | ~185 MB | `3cbbd94b42a76dc80ffa6147babe03d52725cc8cbc40225489343c747a6fb397` |

> 🔒 **Integrity Verification:**  
> Verify downloaded binaries on Linux / macOS via:
> ```bash
> sha256sum app-tv-release.apk
> ```
> Or on Windows PowerShell:
> ```powershell
> Get-FileHash -Algorithm SHA256 app-tv-release.apk
> ```

---

## 📺 How to Install on Android TV / Google TV

### Method 1: Using "Downloader by AFTVnews" (Fastest)
1. Install **Downloader** by AFTVnews from Google Play Store on your TV.
2. Open Downloader and enter the direct APK link or short code into the URL box:
   ```
   https://github.com/b4lol/telyra-releases/releases/download/v1.0.0/app-tv-release.apk
   ```
3. Click **Go** to download and install. When prompted, allow installing unknown apps for Downloader.

### Method 2: Via ADB (Command Line)
Connect your computer to your TV over Wi-Fi:
```bash
adb connect <TV_IP_ADDRESS>:5555
adb install -r app-tv-release.apk
```

### Method 3: USB Flash Drive
1. Download `app-tv-release.apk` to a FAT32/exFAT USB stick.
2. Plug the USB stick into your Android TV box.
3. Open any TV File Manager (such as FX File Explorer or File Commander) and click the APK to install.

---

## 🛡️ Sovereign Security & Privacy Guarantee

1. **Zero Telemetry & Zero Analytics:**  
   TELYRA contains no Google Firebase Analytics, no tracking SDKs, and no advertisement modules.
2. **Hardware-Backed Cryptography:**  
   Your M3U playlists and Xtream Codes credentials never leave your living room. They are sealed with AES-256-GCM via the hardware-backed `AndroidKeyStore` (Titan M / Knox / ARM TrustZone).
3. **Pure Native Player Engine:**  
   Media3 ExoPlayer & LibVLC dual-engine architecture with RFC 7323 4MB TCP socket buffer scaling, zero frame drop guarantee, and 0ms progressive/interlaced bitstream sniffer.

---

## 🐛 Bug Reports & Feature Requests

Found an issue with a specific stream, codec, or Android TV model?  
Please open a ticket on our **[Issue Tracker](https://github.com/b4lol/telyra-releases/issues)** with:
- Device Model (e.g. Nvidia Shield Pro, Chromecast with Google TV, Xiaomi Mi Box S)
- Android OS version (Android 9 / 10 / 11 / 12 / 14)
- Playback engine used (Media3 ExoPlayer or LibVLC)
- Reproducible steps

---

## 📜 Legal Disclaimer

TELYRA is a standalone media player client. It does not host, provide, or bundle any media content, playlists, or IPTV streams. Users are solely responsible for adding their own legitimate media sources.

*© 2026 Hüseyin "b4lol". All rights reserved.*
