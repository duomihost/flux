[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | Tiếng Việt | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 Ứng dụng proxy đa nền tảng mã nguồn mở cho V2Board**

*Cài đặt một dòng · Flutter cho 5 nền tảng · 16 ngôn ngữ*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

---

**Flux** là ứng dụng khách hiện đại được thiết kế cho [V2Board](https://github.com/v2board/v2board).  
Sở hữu ứng dụng thương hiệu của bạn chỉ với **một dòng code**.

</div>

---

## ✨ Tính năng chính

| Tính năng | Mô tả |
|:---:|:---|
| ⚡ **Cài đặt tức thì** | Chỉ cần thay đổi một URL API, không cần phát triển backend |
| 🎨 **Giao diện đẹp** | Material Design 3, hỗ trợ chủ đề tối/sáng |
| 📱 **Đa nền tảng** | Flutter cho Android / iOS / Windows / macOS / Linux |
| 🔐 **Đa giao thức** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Hỗ trợ toàn cầu** | 16 ngôn ngữ |
| 🔓 **Hoàn toàn mã nguồn mở** | Giấy phép MIT, minh bạch và tùy chỉnh được |

---

## 🆚 Tại sao chọn Flux?

| | Flux | Ứng dụng khác |
|:---:|:---:|:---:|
| **Độ khó cài đặt** | 🟢 Một dòng | 🔴 Cần backend |
| **Nền tảng** | 🟢 5 thống nhất | 🟡 Thường 1-2 |
| **Thiết kế UI** | 🟢 Material 3 hiện đại | 🟡 Chức năng ưu tiên |
| **Giao thức** | 🟢 7+ giao thức | 🟡 Hạn chế |
| **Ngôn ngữ** | 🟢 16 ngôn ngữ | 🟡 Chỉ EN/CN |
| **Mã nguồn mở** | 🟢 100% mở | 🔴 Đóng/một phần |
| **Thương hiệu** | 🟢 Dễ rebrand | 🔴 Sửa code |

---

## 📱 Ảnh chụp màn hình

### 📱 Di động

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 Desktop

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 Tùy chỉnh và hỗ trợ thương mại

Nếu bạn cần:
-   🔥 **Thay đổi tên và logo ứng dụng**
-   🎨 **Chủ đề UI tùy chỉnh**
-   🚀 **Thêm tính năng nâng cao**

Liên hệ qua Telegram: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 Giao thức hỗ trợ

✅ **Đã xác minh trên Android và Windows**:
- **Hysteria2**: Giao thức vượt kiểm duyệt nhanh
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 Bắt đầu nhanh

### 1. Clone repository

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. Cấu hình URL API (Quan trọng)

Mở `lib/services/api_config.dart` và sửa:

```dart
Future<String> getBaseUrl() async {
  // Thay đổi thành URL panel của bạn
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. Thay đổi App ID

Thay `com.example.yourapp` bằng App ID của bạn:

| Nền tảng | Đường dẫn file | Trường cần sửa |
|----------|----------------|----------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` và `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` trong `msix_config` |

### 4. Thay đổi icon ứng dụng

1. Chuẩn bị ảnh PNG **1024x1024**
2. Đặt vào `assets/images/app_icon.png`
3. Chạy:
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. Build

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

## ☕ Hỗ trợ dự án

Nếu dự án này giúp ích cho bạn, hãy mời tác giả một ly cà phê!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 Dự án liên quan

### Proxy Engine
-   [Xray-core](https://github.com/XTLS/Xray-core): Engine chính của dự án này
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): Proxy core cổ điển
-   [Hysteria](https://github.com/apernet/hysteria): Giao thức vượt kiểm duyệt mạnh mẽ

### Panel và Quản lý
-   [V2Board](https://github.com/v2board/v2board): Panel V2Ray mạnh mẽ

---

## 💬 Tham gia cộng đồng

- **Nhóm Telegram**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
