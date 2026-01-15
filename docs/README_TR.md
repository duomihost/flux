[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | Türkçe | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 V2Board için Açık Kaynaklı Çapraz Platform Proxy İstemcisi**

*Tek Satır Kurulum · Flutter ile 5 Platform · 16 Dil Desteği*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

---

**Flux**, [V2Board](https://github.com/v2board/v2board) için tasarlanmış modern istemcidir.  
Sadece **tek bir satır kod** değiştirerek markalı uygulamanızı edinin.

</div>

---

## ✨ Ana Özellikler

| Özellik | Açıklama |
|:---:|:---|
| ⚡ **Anında Kurulum** | Sadece bir API URL'si değiştirin, backend geliştirmesi gerekmez |
| 🎨 **Güzel UI** | Material Design 3, koyu/açık tema desteği |
| 📱 **Çapraz Platform** | Flutter ile Android / iOS / Windows / macOS / Linux |
| 🔐 **Çoklu Protokol** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Küresel Destek** | 16 dil |
| 🔓 **Tamamen Açık Kaynak** | MIT Lisansı, şeffaf ve özelleştirilebilir |

---

## 🆚 Neden Flux?

| | Flux | Diğer İstemciler |
|:---:|:---:|:---:|
| **Kurulum Zorluğu** | 🟢 Tek satır | 🔴 Backend gerekli |
| **Platformlar** | 🟢 5 birleşik | 🟡 Genellikle 1-2 |
| **UI Tasarımı** | 🟢 Modern Material 3 | 🟡 İşlevsellik önce |
| **Protokoller** | 🟢 7+ protokol | 🟡 Sınırlı |
| **Diller** | 🟢 16 dil | 🟡 Sadece EN/CN |
| **Açık Kaynak** | 🟢 %100 açık | 🔴 Kapalı/kısmi |
| **Markalama** | 🟢 Kolay rebrand | 🔴 Kod değişikliği |

---

## 📱 Ekran Görüntüleri

### 📱 Mobil

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 Masaüstü

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 Özelleştirme ve Ticari Destek

İhtiyacınız varsa:
-   🔥 **Uygulama adı ve logosu değiştirme**
-   🎨 **Özel UI temaları**
-   🚀 **Gelişmiş özellikler ekleme**

Telegram'dan iletişime geçin: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 Desteklenen Protokoller

✅ **Android ve Windows'ta Doğrulanmış**:
- **Hysteria2**: Hızlı sansür aşma protokolü
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 Hızlı Başlangıç

### 1. Depoyu Klonlayın

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. API URL'sini Yapılandırın (Temel)

`lib/services/api_config.dart` dosyasını açın ve değiştirin:

```dart
Future<String> getBaseUrl() async {
  // Panelinizin URL'sine değiştirin
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. App ID'yi Değiştirin

`com.example.yourapp`'i kendi App ID'nizle değiştirin:

| Platform | Dosya Yolu | Değiştirilecek Alan |
|----------|------------|---------------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` ve `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `msix_config` içinde `identity_name` |

### 4. Uygulama Simgesini Değiştirin

1. **1024x1024** PNG resmi hazırlayın
2. `assets/images/app_icon.png`'e yerleştirin
3. Çalıştırın:
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. Derleyin

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

## ☕ Projeyi Destekleyin

Bu proje size yardımcı olduysa, yazara bir kahve ısmarlayın!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 İlgili Projeler

### Proxy Motorları
-   [Xray-core](https://github.com/XTLS/Xray-core): Bu projenin ana motoru
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): Klasik proxy çekirdeği
-   [Hysteria](https://github.com/apernet/hysteria): Güçlü sansür aşma protokolü

### Paneller ve Yönetim
-   [V2Board](https://github.com/v2board/v2board): Güçlü V2Ray paneli

---

## 💬 Topluluğa Katılın

- **Telegram Grubu**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
