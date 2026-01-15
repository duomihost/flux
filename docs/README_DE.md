[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | Deutsch | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 Plattformübergreifender Open-Source-Proxy-Client für V2Board**

*Einrichtung in einer Zeile · Flutter für 5 Plattformen · 16 Sprachen*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

---

**Flux** ist der moderne Client für [V2Board](https://github.com/v2board/v2board).  
Erhalten Sie Ihre gebrandete App mit nur **einer Codezeile**.

</div>

---

## ✨ Hauptfunktionen

| Funktion | Beschreibung |
|:---:|:---|
| ⚡ **Sofortige Einrichtung** | Nur eine API-URL ändern, kein Backend erforderlich |
| 🎨 **Schöne UI** | Material Design 3, Dark/Light-Theme-Unterstützung |
| 📱 **Plattformübergreifend** | Flutter für Android / iOS / Windows / macOS / Linux |
| 🔐 **Multi-Protokoll** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Globale Unterstützung** | 16 Sprachen |
| 🔓 **Vollständig Open Source** | MIT-Lizenz, transparent und anpassbar |

---

## 🆚 Warum Flux?

| | Flux | Andere Clients |
|:---:|:---:|:---:|
| **Einrichtungsaufwand** | 🟢 Eine Zeile | 🔴 Backend erforderlich |
| **Plattformen** | 🟢 5 vereint | 🟡 Meist 1-2 |
| **UI-Design** | 🟢 Modernes Material 3 | 🟡 Funktion zuerst |
| **Protokolle** | 🟢 7+ Protokolle | 🟡 Begrenzt |
| **Sprachen** | 🟢 16 Sprachen | 🟡 Nur EN/CN |
| **Open Source** | 🟢 100% offen | 🔴 Geschlossen/teilweise |
| **Branding** | 🟢 Einfaches Rebranding | 🔴 Code ändern |

---

## 📱 Screenshots

### 📱 Mobil

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

## 📞 Anpassung und kommerzieller Support

Wenn Sie benötigen:
-   🔥 **App-Name und Logo ändern**
-   🎨 **Benutzerdefinierte UI-Themes**
-   🚀 **Erweiterte Funktionen hinzufügen**

Kontakt auf Telegram: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 Unterstützte Protokolle

✅ **Verifiziert auf Android und Windows**:
- **Hysteria2**: Schnelles Anti-Zensur-Protokoll
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 Schnellstart

### 1. Repository klonen

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. API-URL konfigurieren (Wichtig)

Öffnen Sie `lib/services/api_config.dart` und ändern Sie:

```dart
Future<String> getBaseUrl() async {
  // Ändern Sie zur URL Ihres Panels
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. App-ID ändern

Ersetzen Sie `com.example.yourapp` durch Ihre eigene App-ID:

| Plattform | Dateipfad | Zu änderndes Feld |
|-----------|-----------|-------------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` und `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` in `msix_config` |

### 4. App-Icon ersetzen

1. Bereiten Sie ein **1024x1024** PNG-Bild vor
2. Platzieren Sie es in `assets/images/app_icon.png`
3. Führen Sie aus:
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. Kompilieren

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

## ☕ Projekt unterstützen

Wenn dieses Projekt Ihnen hilft, spendieren Sie dem Autor einen Kaffee!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 Verwandte Projekte

### Proxy-Engines
-   [Xray-core](https://github.com/XTLS/Xray-core): Die Kern-Engine dieses Projekts
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): Klassischer Proxy-Kern
-   [Hysteria](https://github.com/apernet/hysteria): Leistungsstarkes Anti-Zensur-Protokoll

### Panels und Verwaltung
-   [V2Board](https://github.com/v2board/v2board): Leistungsstarkes V2Ray-Panel

---

## 💬 Community beitreten

- **Telegram-Gruppe**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
