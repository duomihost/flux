[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | Português | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 Cliente proxy multiplataforma de código aberto para V2Board**

*Configuração em uma linha · Flutter para 5 plataformas · 16 idiomas*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

💬 **Junte-se à comunidade**: [Grupo do Telegram](https://t.me/+62Otr015kSs1YmNk) · 📞 **Negócios**: [@fluxdeveloper](https://t.me/fluxdeveloper)

---

**Flux** é o cliente moderno projetado para [V2Board](https://github.com/v2board/v2board).  
Tenha seu app com marca própria alterando apenas **uma linha de código**.

</div>

---

## ✨ Recursos principais

| Recurso | Descrição |
|:---:|:---|
| ⚡ **Configuração instantânea** | Apenas modifique uma URL de API, sem desenvolvimento backend |
| 🎨 **Interface bonita** | Material Design 3, suporte a tema escuro/claro |
| 📱 **Multiplataforma** | Flutter para Android / iOS / Windows / macOS / Linux |
| 🔐 **Multi-protocolo** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Suporte global** | 16 idiomas |
| 🔓 **Código aberto completo** | Licença MIT, transparente e personalizável |

---

## 🆚 Por que Flux?

| | Flux | Outros clientes |
|:---:|:---:|:---:|
| **Dificuldade de config.** | 🟢 Uma linha | 🔴 Backend necessário |
| **Plataformas** | 🟢 5 unificadas | 🟡 Geralmente 1-2 |
| **Design UI** | 🟢 Material 3 moderno | 🟡 Funcionalidade primeiro |
| **Protocolos** | 🟢 7+ protocolos | 🟡 Limitado |
| **Idiomas** | 🟢 16 idiomas | 🟡 Apenas EN/CN |
| **Código aberto** | 🟢 100% aberto | 🔴 Fechado/parcial |
| **Personalização** | 🟢 Fácil rebrand | 🔴 Modificar código |

---

## 📱 Capturas de tela

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

## 📞 Personalização e suporte comercial

Se você precisa:
-   🔥 **Mudar nome e logo do app**
-   🎨 **Temas UI personalizados**
-   🚀 **Adicionar recursos avançados**

Contato no Telegram: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 Protocolos suportados

✅ **Verificado em Android e Windows**:
- **Hysteria2**: Protocolo anti-censura rápido
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 Início rápido

### 1. Clonar o repositório

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. Configurar URL da API (Essencial)

Abra `lib/services/api_config.dart` e modifique:

```dart
Future<String> getBaseUrl() async {
  // Mude para a URL do seu painel
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. Mudar App ID

Substitua `com.example.yourapp` pelo seu próprio App ID:

| Plataforma | Caminho do arquivo | Campo a modificar |
|------------|-------------------|-------------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` e `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` em `msix_config` |

### 4. Substituir ícone do app

1. Prepare uma imagem PNG **1024x1024**
2. Coloque em `assets/images/app_icon.png`
3. Execute:
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

## ☕ Apoie o projeto

Se este projeto te ajudou, pague um café para o autor!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 Projetos relacionados

### Motores de proxy
-   [Xray-core](https://github.com/XTLS/Xray-core): Motor principal deste projeto
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): Núcleo proxy clássico
-   [Hysteria](https://github.com/apernet/hysteria): Poderoso protocolo anti-censura

### Painéis e gestão
-   [V2Board](https://github.com/v2board/v2board): Poderoso painel V2Ray

---

## 💬 Junte-se à comunidade

- **Grupo do Telegram**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
