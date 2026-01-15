[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | Español | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 Cliente proxy multiplataforma de código abierto para V2Board**

*Configuración en una línea · Flutter para 5 plataformas · 16 idiomas*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

---

**Flux** es el cliente moderno diseñado para [V2Board](https://github.com/v2board/v2board).  
Obtén tu app con marca propia cambiando solo **una línea de código**.

</div>

---

## ✨ Características principales

| Característica | Descripción |
|:---:|:---|
| ⚡ **Configuración instantánea** | Solo modifica una URL de API, sin desarrollo backend |
| 🎨 **Interfaz hermosa** | Material Design 3, soporte tema oscuro/claro |
| 📱 **Multiplataforma** | Flutter para Android / iOS / Windows / macOS / Linux |
| 🔐 **Multi-protocolo** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Soporte global** | 16 idiomas |
| 🔓 **Código abierto completo** | Licencia MIT, transparente y personalizable |

---

## 🆚 ¿Por qué Flux?

| | Flux | Otros clientes |
|:---:|:---:|:---:|
| **Dificultad de config.** | 🟢 Una línea | 🔴 Backend requerido |
| **Plataformas** | 🟢 5 unificadas | 🟡 Usualmente 1-2 |
| **Diseño UI** | 🟢 Material 3 moderno | 🟡 Funcionalidad primero |
| **Protocolos** | 🟢 7+ protocolos | 🟡 Limitado |
| **Idiomas** | 🟢 16 idiomas | 🟡 Solo EN/CN |
| **Código abierto** | 🟢 100% abierto | 🔴 Cerrado/parcial |
| **Personalización** | 🟢 Fácil rebrand | 🔴 Modificar código |

---

## 📱 Capturas de pantalla

### 📱 Móvil

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 Escritorio

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 Personalización y soporte comercial

Si necesitas:
-   🔥 **Cambiar nombre y logo de la app**
-   🎨 **Temas UI personalizados**
-   🚀 **Agregar funciones avanzadas**

Contacta en Telegram: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 Protocolos soportados

✅ **Verificado en Android y Windows**:
- **Hysteria2**: Protocolo anti-censura rápido
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 Inicio rápido

### 1. Clonar el repositorio

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. Configurar URL de API (Esencial)

Abre `lib/services/api_config.dart` y modifica:

```dart
Future<String> getBaseUrl() async {
  // Cambia a la URL de tu panel
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. Cambiar App ID

Reemplaza `com.example.yourapp` con tu propio App ID:

| Plataforma | Ruta del archivo | Campo a modificar |
|------------|------------------|-------------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` y `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` en `msix_config` |

### 4. Reemplazar icono de la app

1. Prepara una imagen PNG **1024x1024**
2. Colócala en `assets/images/app_icon.png`
3. Ejecuta:
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. Compilar

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

## ☕ Apoya el proyecto

Si este proyecto te ayuda, ¡invita al autor a un café!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 Proyectos relacionados

### Motores de proxy
-   [Xray-core](https://github.com/XTLS/Xray-core): Motor principal de este proyecto
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): Núcleo proxy clásico
-   [Hysteria](https://github.com/apernet/hysteria): Potente protocolo anti-censura

### Paneles y gestión
-   [V2Board](https://github.com/v2board/v2board): Potente panel V2Ray

---

## 💬 Únete a la comunidad

- **Grupo de Telegram**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
