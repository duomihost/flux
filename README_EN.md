[English](README_EN.md) | [简体中文](README.md) | [繁體中文](docs/README_TW.md) | [日本語](docs/README_JA.md) | [한국어](docs/README_KO.md) | [Русский](docs/README_RU.md) | [हिन्दी](docs/README_HI.md) | [Español](docs/README_ES.md) | [Português](docs/README_PT.md) | [Français](docs/README_FR.md) | [Deutsch](docs/README_DE.md) | [العربية](docs/README_AR.md) | [Türkçe](docs/README_TR.md) | [Tiếng Việt](docs/README_VI.md) | [ไทย](docs/README_TH.md) | [Indonesia](docs/README_ID.md)

<div align="center">

# ⚡ Flux

### White-Label Client Solution for V2Board Operators

**Flutter-based cross-platform proxy client, built for airport/VPN service providers**

Change one API URL → Build → Get your branded app

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)

💬 [Join Telegram Group](https://t.me/+62Otr015kSs1YmNk) · 📞 [Business @fluxdeveloper](https://t.me/fluxdeveloper)

</div>

---

## 🎯 What is Flux?

> **Flux is NOT a VPN app for end users. It's an open-source solution for VPN/proxy service providers to build their own branded client.**

If you're running a V2Board panel, you've probably faced these problems:

- 😫 Users complain that third-party clients are ugly or complicated
- 😫 You want your own branded app but don't know how to develop one
- 😫 Outsourcing is too expensive, open-source projects are hard to customize

**Flux solves all of these.**

---

## 👥 Who is Flux for?

| User Type | Your Need | How Flux Helps |
|:---:|:---|:---|
| 🛫 **Service Providers** | Need a branded client ASAP | ✅ Change one line, build in 5 minutes |
| 🧑‍💻 **Developers** | Looking for a clean Flutter proxy project to fork | ✅ MIT license, free for commercial use |
| 👤 **End Users** | Want a beautiful, modern proxy client | ✅ Contact your VPN provider for their branded app |

---

## 🆚 Why Flux? (vs Competitors)

| Feature | Flux | v2rayNG | Clash | Shadowrocket |
|:---|:---:|:---:|:---:|:---:|
| **Cross-platform** | ✅ 5 platforms | ❌ Android only | ⚠️ Multiple clients | ❌ iOS only |
| **V2Board API Native** | ✅ Built-in | ❌ Manual import | ❌ Manual import | ❌ Manual import |
| **Flutter Modern UI** | ✅ Material 3 | ❌ Native Android | ❌ Web-style | ❌ Native iOS |
| **White-label Ready** | ✅ Out of box | ❌ Needs source mod | ❌ Difficult | ❌ Impossible |
| **Commercial Use** | ✅ MIT License | ✅ | ⚠️ | ❌ |
| **Open Source** | ✅ 100% | ✅ | ⚠️ Partial | ❌ |

**👉 Bottom line: Flux is the ONLY white-label-ready, commercially-usable, open-source V2Board client.**

---

## ⚡ Get Started in 5 Minutes

```bash
# 1. Clone
git clone https://github.com/flux-apphub/flux.git
cd flux

# 2. Install dependencies
flutter pub get

# 3. Change ONE line (put your panel URL)
# Open lib/services/api_config.dart, modify:
# return 'https://your-panel.com/api/v1';

# 4. Run
flutter run
```

**Done. Your branded V2Board client is running.**

---

## 📱 Screenshots

<details>
<summary>📱 Click to view mobile screenshots</summary>

| | | |
| :---: | :---: | :---: |
| <img src="assets/images/screenshots/1.png" width="200"> | <img src="assets/images/screenshots/2.png" width="200"> | <img src="assets/images/screenshots/3.png" width="200"> |
| <img src="assets/images/screenshots/4.png" width="200"> | <img src="assets/images/screenshots/5.png" width="200"> | |

</details>

<details>
<summary>💻 Click to view desktop screenshots</summary>

| | |
| :---: | :---: |
| <img src="assets/images/screenshots/6.png" width="400"> | <img src="assets/images/screenshots/7.png" width="400"> |
| <img src="assets/images/screenshots/8.png" width="400"> | <img src="assets/images/screenshots/9.png" width="400"> |

</details>

---

## 🛠 Supported Protocols

| Protocol | Status | Notes |
|:---|:---:|:---|
| **Hysteria2** | ✅ Verified | Ultra-fast anti-blocking |
| **VLESS Reality** | ✅ Verified | Latest anti-detection tech |
| **VMess** | ✅ Verified | TCP / WebSocket |
| **Trojan** | ✅ Verified | - |
| **Shadowsocks** | ✅ Verified | AEAD encryption |

> ⚠️ iOS/macOS not fully tested (developer has no Apple devices). Community contributions welcome!

---

## 🎨 Customization Guide (for Providers)

### Rebrand in 3 steps:

**Step 1: Change App ID**

| Platform | File | What to change |
|:---|:---|:---|
| Android | `android/app/build.gradle.kts` | `applicationId` |
| iOS | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| macOS | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| Windows | `pubspec.yaml` | `msix_config.identity_name` |
| Linux | `linux/CMakeLists.txt` | `APPLICATION_ID` |

**Step 2: Change App Name**

| Platform | File | What to change |
|:---|:---|:---|
| Android | `AndroidManifest.xml` | `android:label` |
| iOS | `Info.plist` | `CFBundleDisplayName` |
| Windows | `Runner.rc` | `ProductName` |

**Step 3: Replace Icon**

```bash
# Put your 1024x1024 PNG at assets/images/app_icon.png
flutter pub run flutter_launcher_icons
```

**Done. You now have a branded proxy client.**

---

## 💰 Commercial Services

Need help? We offer:

| Service | Description |
|:---|:---|
| 🔥 **Quick Build** | We compile Android/iOS/Windows packages for you |
| 🎨 **UI Customization** | Colors, layout, extra features |
| 🔐 **Licensing System** | Device authorization, expiry alerts |

**Contact:** [@fluxdeveloper](https://t.me/fluxdeveloper)

---

## 🔧 Architecture (for Developers)

<details>
<summary>Click to expand technical details</summary>

### Core Stack

- **UI**: Flutter 3.x + Material Design 3
- **Logic**: `UnifiedVpnService` router
- **Core**: V2Ray / Xray Core

### Platform Implementation

| Platform | Mechanism | Notes |
|:---|:---|:---|
| Android | `VpnService` API | TUN mode, no root |
| iOS | `NetworkExtension` | Packet Tunnel Provider |
| Desktop | System Proxy + Sidecar | Proxy + core process |

### Project Structure

```
lib/
├── main.dart          # Entry
├── screens/           # Pages
├── services/          # Core services
│   ├── api_config.dart    # 👈 Change this!
│   ├── v2ray_service.dart
│   └── vpn_service.dart
├── models/            # Data models
└── widgets/           # Components
```

</details>

---

## 🔗 Related Projects

- [Xray-core](https://github.com/XTLS/Xray-core) - Core engine
- [V2Board](https://github.com/v2board/v2board) - Panel
- [hev-socks5-tunnel](https://github.com/heiher/hev-socks5-tunnel) - High-performance SOCKS5 tunnel

---

## ☕ Sponsor

If Flux saved you development costs, consider buying me a coffee:

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) |
| :---: | :---: | :---: |
| <img src="assets/images/donation/usdt_trc20.png" width="150"> | <img src="assets/images/donation/usdc_arbitrum.png" width="150"> | <img src="assets/images/donation/eth_arbitrum.png" width="150"> |

---

## 📄 License

MIT License - Free to use, modify, distribute and commercialize.

---

<div align="center">

**Flux** - White-label client for V2Board providers

*Keywords: V2Board client, airport client, Flutter proxy, white-label VPN, open source proxy*

</div>
