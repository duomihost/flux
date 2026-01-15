[English](README_EN.md) | [简体中文](README.md) | [繁體中文](docs/README_TW.md) | [日本語](docs/README_JA.md) | [한국어](docs/README_KO.md) | [Русский](docs/README_RU.md) | [हिन्दी](docs/README_HI.md) | [Español](docs/README_ES.md) | [Português](docs/README_PT.md) | [Français](docs/README_FR.md) | [Deutsch](docs/README_DE.md) | [العربية](docs/README_AR.md) | [Türkçe](docs/README_TR.md) | [Tiếng Việt](docs/README_VI.md) | [ไทย](docs/README_TH.md) | [Indonesia](docs/README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 The Modern Open-Source V2Board Client Built with Flutter**

*One-Line Setup · 5 Platforms · 16 Languages · Beautiful UI*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

---

**Flux** is the ultimate cross-platform client for [V2Board](https://github.com/v2board/v2board).  
Deploy your branded VPN app in minutes — just change **one line of code**.

</div>

---

## ✨ Key Features

| Feature | Description |
|:---:|:---|
| ⚡ **Instant Setup** | Just modify one API URL, no backend development required |
| 🎨 **Beautiful UI** | Material Design 3 with dark/light theme support |
| 📱 **Cross-Platform** | Built with Flutter for Android / iOS / Windows / macOS / Linux |
| 🔐 **Multi-Protocol** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Localization** | 16 languages covering global markets |
| 🔓 **Fully Open Source** | MIT License, transparent and customizable |

---

## 🆚 Why Flux?

| | Flux | Other Clients |
|:---:|:---:|:---:|
| **Setup Difficulty** | 🟢 One line change | 🔴 Backend required |
| **Platform Support** | 🟢 5 platforms unified | 🟡 Usually 1-2 |
| **UI Design** | 🟢 Modern Material 3 | 🟡 Function-first |
| **Protocol Coverage** | 🟢 7+ protocols | 🟡 Limited |
| **Languages** | 🟢 16 languages | 🟡 EN/CN only |
| **Open Source** | 🟢 100% open | 🔴 Closed/partial |
| **Branding** | 🟢 Easy rebrand | 🔴 Source modification |

---

## 📱 Screenshots

### 📱 Mobile

| | | |
| :---: | :---: | :---: |
| <img src="assets/images/screenshots/1.png" width="200"> | <img src="assets/images/screenshots/2.png" width="200"> | <img src="assets/images/screenshots/3.png" width="200"> |
| <img src="assets/images/screenshots/4.png" width="200"> | <img src="assets/images/screenshots/5.png" width="200"> | |

### 💻 Desktop

| | |
| :---: | :---: |
| <img src="assets/images/screenshots/6.png" width="400"> | <img src="assets/images/screenshots/7.png" width="400"> |
| <img src="assets/images/screenshots/8.png" width="400"> | <img src="assets/images/screenshots/9.png" width="400"> |

---

## 📞 Customization & Commercial Support

If you need:
-   🔥 **Modify App name and Logo**
-   🎨 **Custom UI themes**
-   🚀 **Add advanced features**

Contact on Telegram: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🔧 Technical Architecture

Flux is not just a simple UI wrapper - it integrates a powerful routing core to ensure stable cross-platform connections.

### 1. Core Architecture

*   **UI Layer**: Built with **Flutter**, one codebase for 5 platforms.
*   **Logic Layer**: `UnifiedVpnService` dispatches traffic based on running platform.
*   **Core Layer**: Built-in **V2Ray / Xray Core** for protocol handling, encryption and routing.

### 2. Traffic Forwarding

Flux uses native system-level solutions on each platform:

#### 🤖 Android
*   **Mechanism**: Native Android **`VpnService`** API.
*   **How**: Creates a virtual TUN interface. Uses **JNI** to call the routing core.
*   **Advantage**: Global proxy without root.

#### 🍎 iOS
*   **Mechanism**: Apple **`NetworkExtension` (Packet Tunnel Provider)** framework.
*   **How**: Runs an isolated VPN process (`PacketTunnelProvider.swift`).
*   **Advantage**: Battery efficient, App Store compliant.

#### 💻 Desktop (Windows / macOS / Linux)
*   **Mechanism**: **System Proxy** + **Sidecar Process**.
*   **How**: Launches Xray core in background, configures system HTTP/SOCKS5 proxy.
*   **Advantage**: Good compatibility, no driver modification needed.

### 🛠 Supported Protocols

✅ **Verified on Android & Windows**:
- **Hysteria2**: [https://v2.hysteria.network/](https://v2.hysteria.network/)
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)

⚠️ **Note**: Developer has no Apple devices, **iOS and macOS builds are not fully tested**. Community contributions welcome!

---

## 🌐 OSS Remote Configuration

Flux supports remote configuration via OSS/CDN for **automatic domain failover**, **version updates**, **announcements**, and more.

### Setup

1. Upload the JSON config file to your OSS/CDN (Alibaba Cloud OSS, Cloudflare R2, GitHub Raw, etc.)
2. Configure `_ossUrls` in `lib/services/remote_config_service.dart`

### JSON Configuration Format

```json
{
  "config_version": 1,
  "domains": [
    "https://api1.example.com/api/v1",
    "https://api2.example.com/api/v1"
  ],
  "backup_subscription": "https://backup-sub.example.com/sub",
  
  "announcement": {
    "enabled": true,
    "title": "System Notice",
    "content": "Service is running normally.",
    "type": "info"
  },
  
  "maintenance": {
    "enabled": false,
    "message": "System maintenance in progress"
  },
  
  "update": {
    "min_version": "1.0.0",
    "latest": {
      "android": { "version": "1.2.0", "url": "https://example.com/flux-1.2.0.apk", "force": false },
      "ios": { "version": "1.2.0", "url": "https://apps.apple.com/app/id123456", "force": false },
      "windows": { "version": "1.2.0", "url": "https://example.com/flux-1.2.0-win.zip", "force": false },
      "macos": { "version": "1.2.0", "url": "https://example.com/flux-1.2.0-mac.dmg", "force": false },
      "linux": { "version": "1.2.0", "url": "https://example.com/flux-1.2.0-linux.tar.gz", "force": false }
    },
    "changelog": "1. Added WireGuard and TUIC support\n2. Bug fixes"
  },
  
  "contact": {
    "telegram": "https://t.me/your_group",
    "website": "https://yoursite.com"
  },
  
  "features": {
    "invite_enabled": true,
    "purchase_enabled": true,
    "ssr_enabled": false
  },
  
  "recommended_nodes": ["HongKong01", "Japan02"]
}
```

### Field Descriptions

| Field | Description |
|-------|-------------|
| `config_version` | Config version number for cache validation |
| `domains` | API domain list, in priority order, auto-tested for availability |
| `backup_subscription` | Backup subscription URL |
| `announcement` | Announcement config, `type` can be `info`/`warning`/`error` |
| `maintenance` | Maintenance mode, blocks user operations when enabled |
| `update` | Version update info, `force: true` for mandatory update |
| `min_version` | Minimum supported version, older versions forced to update |
| `contact` | Customer support links |
| `features` | Feature toggles |
| `recommended_nodes` | Recommended node names |

---

### 💬 Community

- **Telegram Group**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. Configure API URL (Essential)

Open `lib/services/api_config.dart` and modify:

```dart
Future<String> getBaseUrl() async {
  // Change this to your panel URL
  // Example: https://v2board.com -> https://v2board.com/api/v1
  // Note: Keep the /api/v1 suffix
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. Modify App ID (Required)

Replace `com.example.yourapp` with your own App ID (e.g., `com.yourname.project`):

| Platform | File Path | Field to Modify |
|----------|-----------|-----------------| 
| **Android** | `android/app/build.gradle.kts` | `applicationId` and `namespace` |
| **Android** | `android/app/src/main/AndroidManifest.xml` | Check package declaration |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` (search and replace all) |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` under `msix_config` |

> ⚠️ **Important**: After modifying Android package name, rename the directory structure `android/app/src/main/kotlin/com/example/yourapp/` accordingly.

---

### 4. Modify App Name

| Platform | File Path | Field to Modify |
|----------|-----------|-----------------| 
| **Android** | `android/app/src/main/AndroidManifest.xml` | `android:label="YourAppName"` |
| **iOS** | `ios/Runner/Info.plist` | `CFBundleDisplayName` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_NAME` |
| **Linux** | `linux/CMakeLists.txt` | `set(BINARY_NAME "YourAppName")` |
| **Windows** | `windows/runner/Runner.rc` | `VALUE "ProductName"` and `VALUE "FileDescription"` |
| **Windows** | `pubspec.yaml` | `display_name` under `msix_config` |

---

### 5. Replace App Icon 🎨

#### Method 1: Using flutter_launcher_icons (Recommended)

1. Prepare a **1024x1024** PNG image (square, no transparency preferred)
2. Place it at `assets/images/app_icon.png`
3. Ensure `pubspec.yaml` contains:
   ```yaml
   dev_dependencies:
     flutter_launcher_icons: ^0.14.4

   flutter_launcher_icons:
     android: true
     ios: true
     image_path: "assets/images/app_icon.png"
     remove_alpha_ios: true
   ```
4. Run:
   ```bash
   flutter pub run flutter_launcher_icons
   ```

#### Method 2: Manual Replacement

| Platform | Icon Location | Notes |
|----------|---------------|-------|
| **Android** | `android/app/src/main/res/mipmap-*/` | Replace all `ic_launcher.png` sizes |
| **iOS** | `ios/Runner/Assets.xcassets/AppIcon.appiconset/` | Replace all icon files |
| **macOS** | `macos/Runner/Assets.xcassets/AppIcon.appiconset/` | Same as iOS |
| **Windows** | `windows/runner/resources/app_icon.ico` | Requires `.ico` format |
| **Linux** | `assets/icons/app_icon.png` | Or configure in `linux/CMakeLists.txt` |

> 💡 **Tip**: Use [https://icon.kitchen](https://icon.kitchen) or [https://appicon.co](https://appicon.co) to generate icons for all platforms.

---

### 6. Other Customizations

#### Modify Splash Screen

| Platform | File Location | Description |
|----------|---------------|-------------|
| **Android** | `android/app/src/main/res/drawable/splash_icon.xml` | Splash icon SVG |
| **Android** | `android/app/src/main/res/values/colors.xml` | Background color |
| **iOS** | `ios/Runner/Assets.xcassets/LaunchImage.imageset/` | Launch images |
| **iOS** | `ios/Runner/Base.lproj/LaunchScreen.storyboard` | Launch screen layout |

#### Modify Theme Colors

File: `lib/main.dart` or `lib/theme/` directory
```dart
MaterialApp(
  theme: ThemeData(
    primarySwatch: Colors.blue,  // Change to your brand color
    colorScheme: ColorScheme.fromSeed(seedColor: Colors.blue),
  ),
)
```

#### Configure OSS Remote Config URL

File: `lib/services/remote_config_service.dart`
```dart
static const List<String> _ossUrls = [
  'https://your-bucket.oss-cn-hangzhou.aliyuncs.com/config.json',
  'https://cdn.example.com/config.json',
];
```

### 7. Build

Ensure Flutter is installed.

-   **Android (APK)**:
    ```bash
    flutter build apk --release
    ```
    *Output: `build/app/outputs/flutter-apk/app-release.apk`*

-   **iOS (IPA)**:
    ```bash
    flutter build ipa
    ```
    *Requires macOS and Apple Developer account.*
    *Output: `build/ios/archive/Runner.xcarchive`*

-   **Windows (exe)**:
    ```bash
    flutter build windows
    ```
    *Output: `build/windows/runner/Release/`*

-   **macOS (app)**:
    ```bash
    flutter build macos
    ```
    *Output: `build/macos/Build/Products/Release/flux.app`*

-   **Linux**:
    ```bash
    flutter build linux
    ```
    *Output: `build/linux/x64/release/bundle/`*

---

## ☕ Support the Project

If this project helps you, consider buying the author a coffee!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 Related Projects

### Core Proxy Engines
-   [Xray-core](https://github.com/XTLS/Xray-core): The core proxy engine used by this project.
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): Classic proxy core.
-   [Sing-box](https://github.com/SagerNet/sing-box): Universal proxy platform.
-   [Hysteria](https://github.com/apernet/hysteria): Powerful anti-censorship proxy protocol.

### Panels & Management
-   [V2Board](https://github.com/v2board/v2board): Powerful V2Ray panel.

### Tools & Libraries
-   [hev-socks5-tunnel](https://github.com/heiher/hev-socks5-tunnel): High-performance SOCKS5 tunnel.
-   [geoip](https://github.com/Loyalsoldier/geoip): GeoIP database.
-   [domain-list-community](https://github.com/v2fly/domain-list-community): Domain routing rules.

### Other Client References
-   [v2rayNG](https://github.com/2dust/v2rayNG): Android V2Ray client.
-   [V2RayXS](https://github.com/tzmax/V2RayXS): macOS V2Ray client.
-   [NekoBox](https://github.com/MatsuriDayo/NekoBoxForAndroid): Multi-protocol proxy client.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

*Keywords: V2Board client, Flutter VPN app, V2Ray Xray client, cross-platform proxy, Hysteria2 VLESS VMess Shadowsocks Trojan*

</div>
