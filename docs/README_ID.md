[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | Indonesia

<div align="center">

# ⚡ Flux

**🚀 Klien Proxy Lintas Platform Open Source untuk V2Board**

*Setup Satu Baris · Flutter untuk 5 Platform · 16 Bahasa*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

💬 **Bergabung dengan Komunitas**: [Grup Telegram](https://t.me/+62Otr015kSs1YmNk) · 📞 **Bisnis**: [@fluxdeveloper](https://t.me/fluxdeveloper)

---

**Flux** adalah klien modern yang dirancang untuk [V2Board](https://github.com/v2board/v2board).  
Dapatkan aplikasi bermerek Anda hanya dengan mengubah **satu baris kode**.

</div>

---

## ✨ Fitur Utama

| Fitur | Deskripsi |
|:---:|:---|
| ⚡ **Setup Instan** | Hanya ubah satu URL API, tidak perlu pengembangan backend |
| 🎨 **UI Cantik** | Material Design 3, dukungan tema gelap/terang |
| 📱 **Lintas Platform** | Flutter untuk Android / iOS / Windows / macOS / Linux |
| 🔐 **Multi-Protokol** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Dukungan Global** | 16 bahasa |
| 🔓 **Sepenuhnya Open Source** | Lisensi MIT, transparan dan dapat disesuaikan |

---

## 🆚 Mengapa Flux?

| | Flux | Klien Lain |
|:---:|:---:|:---:|
| **Kesulitan Setup** | 🟢 Satu baris | 🔴 Butuh backend |
| **Platform** | 🟢 5 terpadu | 🟡 Biasanya 1-2 |
| **Desain UI** | 🟢 Material 3 modern | 🟡 Fungsi dulu |
| **Protokol** | 🟢 7+ protokol | 🟡 Terbatas |
| **Bahasa** | 🟢 16 bahasa | 🟡 Hanya EN/CN |
| **Open Source** | 🟢 100% terbuka | 🔴 Tertutup/parsial |
| **Branding** | 🟢 Rebrand mudah | 🔴 Ubah kode |

---

## 📱 Screenshot

### 📱 Mobile

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

## 📞 Kustomisasi dan Dukungan Komersial

Jika Anda butuh:
-   🔥 **Ubah nama dan logo aplikasi**
-   🎨 **Tema UI kustom**
-   🚀 **Tambah fitur lanjutan**

Hubungi di Telegram: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 Protokol yang Didukung

✅ **Diverifikasi di Android dan Windows**:
- **Hysteria2**: Protokol bypass sensor cepat
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 Mulai Cepat

### 1. Clone Repository

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. Konfigurasi URL API (Penting)

Buka `lib/services/api_config.dart` dan ubah:

```dart
Future<String> getBaseUrl() async {
  // Ubah ke URL panel Anda
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. Ubah App ID

Ganti `com.example.yourapp` dengan App ID Anda:

| Platform | Path File | Field yang Diubah |
|----------|-----------|-------------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` dan `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` di `msix_config` |

### 4. Ganti Ikon Aplikasi

1. Siapkan gambar PNG **1024x1024**
2. Letakkan di `assets/images/app_icon.png`
3. Jalankan:
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

## ☕ Dukung Proyek

Jika proyek ini membantu Anda, traktir penulis secangkir kopi!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 Proyek Terkait

### Proxy Engine
-   [Xray-core](https://github.com/XTLS/Xray-core): Engine utama proyek ini
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): Proxy core klasik
-   [Hysteria](https://github.com/apernet/hysteria): Protokol anti-sensor yang kuat

### Panel dan Manajemen
-   [V2Board](https://github.com/v2board/v2board): Panel V2Ray yang powerful

---

## 💬 Bergabung dengan Komunitas

- **Grup Telegram**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
