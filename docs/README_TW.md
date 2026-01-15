[English](../README_EN.md) | [简体中文](../README.md) | 繁體中文 | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 為 V2Board 而生的開源跨平台代理客戶端**

*一行程式碼完成對接 · Flutter 五端統一 · 16 種語言支援*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

💬 **加入社群**: [Telegram 群組](https://t.me/+62Otr015kSs1YmNk) · 📞 **商務合作**: [@fluxdeveloper](https://t.me/fluxdeveloper)

---

**Flux** 是專為 [V2Board](https://github.com/v2board/v2board) 設計的現代化客戶端。  
無論您是運營商還是開發者，只需修改 **一行 API 地址**，即可擁有專屬品牌 App。

</div>

---

## ✨ 核心亮點

| 亮點 | 描述 |
|:---:|:---|
| ⚡ **極速對接** | 只需修改一行 API 地址，無需任何後端開發經驗 |
| 🎨 **精美 UI** | Material Design 3 風格，支援深色/淺色主題 |
| 📱 **全平台覆蓋** | Flutter 構建，Android / iOS / Windows / macOS / Linux 一套程式碼 |
| 🔐 **多協定支援** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **全球本地化** | 16 種語言，覆蓋中日韓英俄法德西葡越泰印土阿 |
| 🔓 **完全開源** | MIT 協議，程式碼透明，自由客製 |

---

## 🆚 為什麼選擇 Flux？

| | Flux | 傳統客戶端 |
|:---:|:---:|:---:|
| **對接難度** | 🟢 改一行程式碼 | 🔴 需後端開發 |
| **平台支援** | 🟢 5 端統一 | 🟡 通常 1-2 端 |
| **UI 設計** | 🟢 現代 Material 3 | 🟡 功能優先 |
| **協定覆蓋** | 🟢 7+ 主流協定 | 🟡 有限支援 |
| **多語言** | 🟢 16 種語言 | 🟡 中英為主 |
| **開源程度** | 🟢 100% 開源 | 🔴 閉源或部分開源 |
| **品牌客製** | 🟢 輕鬆換名換圖示 | 🔴 需改原始碼 |

---

## 📱 介面預覽

### 📱 App 版本

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 桌面版本

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 客製化與商業支援

如果您需要：
-   🔥 **修改 App 名稱和 Logo**
-   🎨 **客製專屬 UI 主題**
-   🚀 **增加進階功能**

請透過 Telegram 聯繫：👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 支援協定

✅ **已驗證平台 (Android & Windows)**:
- **Hysteria2**: 極速抗封鎖協定
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 快速開始

### 1. 下載程式碼

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. 替換 API 網址 (核心步驟)

開啟 `lib/services/api_config.dart`，修改：

```dart
Future<String> getBaseUrl() async {
  // 改為您的面板網址
  return 'https://您的面板網域.com/api/v1'; 
}
```

### 3. 修改 App ID

將 `com.example.yourapp` 替換為您自己的 App ID：

| 平台 | 檔案路徑 | 修改項 |
|------|---------|--------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` 和 `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `msix_config` 下的 `identity_name` |

### 4. 替換應用程式圖示

1. 準備一張 **1024x1024** 的 PNG 圖片
2. 放到 `assets/images/app_icon.png`
3. 執行：
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. 開始打包

```bash
# Android
flutter build apk --release

# iOS
flutter build ipa

# Windows
flutter build windows

# macOS
flutter build macos

# Linux
flutter build linux
```

---

## ☕ 請我喝杯咖啡

如果這個專案對您有幫助，歡迎請作者喝杯咖啡，支持開源開發！

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 相關專案

### 核心代理引擎
-   [Xray-core](https://github.com/XTLS/Xray-core): 本專案使用的核心代理引擎
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): 經典的代理核心
-   [Hysteria](https://github.com/apernet/hysteria): 強大的抗封鎖代理協定

### 面板 & 管理
-   [V2Board](https://github.com/v2board/v2board): 強大的 V2Ray 面板

---

## 💬 加入社群

- **Telegram 群組**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
