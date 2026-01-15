[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | Français | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 Client proxy multiplateforme open source pour V2Board**

*Configuration en une ligne · Flutter pour 5 plateformes · 16 langues*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

---

**Flux** est le client moderne conçu pour [V2Board](https://github.com/v2board/v2board).  
Obtenez votre application personnalisée en changeant seulement **une ligne de code**.

</div>

---

## ✨ Fonctionnalités clés

| Fonctionnalité | Description |
|:---:|:---|
| ⚡ **Configuration instantanée** | Modifiez une seule URL API, pas de développement backend requis |
| 🎨 **Belle interface** | Material Design 3, support thème sombre/clair |
| 📱 **Multiplateforme** | Flutter pour Android / iOS / Windows / macOS / Linux |
| 🔐 **Multi-protocole** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Support mondial** | 16 langues |
| 🔓 **Entièrement open source** | Licence MIT, transparent et personnalisable |

---

## 🆚 Pourquoi Flux ?

| | Flux | Autres clients |
|:---:|:---:|:---:|
| **Difficulté config.** | 🟢 Une ligne | 🔴 Backend requis |
| **Plateformes** | 🟢 5 unifiées | 🟡 Généralement 1-2 |
| **Design UI** | 🟢 Material 3 moderne | 🟡 Fonctionnalité d'abord |
| **Protocoles** | 🟢 7+ protocoles | 🟡 Limité |
| **Langues** | 🟢 16 langues | 🟡 EN/CN seulement |
| **Open source** | 🟢 100% ouvert | 🔴 Fermé/partiel |
| **Personnalisation** | 🟢 Rebranding facile | 🔴 Modifier le code |

---

## 📱 Captures d'écran

### 📱 Mobile

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 Bureau

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 Personnalisation et support commercial

Si vous avez besoin de :
-   🔥 **Changer le nom et le logo de l'app**
-   🎨 **Thèmes UI personnalisés**
-   🚀 **Ajouter des fonctionnalités avancées**

Contactez sur Telegram : 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 Protocoles supportés

✅ **Vérifié sur Android et Windows** :
- **Hysteria2** : Protocole anti-censure rapide
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 Démarrage rapide

### 1. Cloner le dépôt

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. Configurer l'URL API (Essentiel)

Ouvrez `lib/services/api_config.dart` et modifiez :

```dart
Future<String> getBaseUrl() async {
  // Changez pour l'URL de votre panneau
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. Modifier l'App ID

Remplacez `com.example.yourapp` par votre propre App ID :

| Plateforme | Chemin du fichier | Champ à modifier |
|------------|-------------------|------------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` et `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` dans `msix_config` |

### 4. Remplacer l'icône de l'app

1. Préparez une image PNG **1024x1024**
2. Placez-la dans `assets/images/app_icon.png`
3. Exécutez :
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. Compiler

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

## ☕ Soutenez le projet

Si ce projet vous aide, offrez un café à l'auteur !

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 Projets connexes

### Moteurs proxy
-   [Xray-core](https://github.com/XTLS/Xray-core) : Moteur principal de ce projet
-   [V2Ray-core](https://github.com/v2fly/v2ray-core) : Noyau proxy classique
-   [Hysteria](https://github.com/apernet/hysteria) : Puissant protocole anti-censure

### Panneaux et gestion
-   [V2Board](https://github.com/v2board/v2board) : Puissant panneau V2Ray

---

## 💬 Rejoignez la communauté

- **Groupe Telegram** : [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
