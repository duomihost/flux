[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | Русский | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 Кроссплатформенный прокси-клиент с открытым исходным кодом для V2Board**

*Настройка в одну строку · Flutter для 5 платформ · Поддержка 16 языков*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

💬 **Присоединяйтесь**: [Telegram группа](https://t.me/+62Otr015kSs1YmNk) · 📞 **Бизнес**: [@fluxdeveloper](https://t.me/fluxdeveloper)

---

**Flux** — современный клиент, разработанный для [V2Board](https://github.com/v2board/v2board).  
Получите своё брендированное приложение, изменив всего **одну строку API**.

</div>

---

## ✨ Ключевые особенности

| Особенность | Описание |
|:---:|:---|
| ⚡ **Мгновенная настройка** | Измените только один URL API, бэкенд не требуется |
| 🎨 **Красивый UI** | Material Design 3, поддержка тёмной/светлой темы |
| 📱 **Кроссплатформенность** | Flutter для Android / iOS / Windows / macOS / Linux |
| 🔐 **Мультипротокол** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **Глобальная поддержка** | 16 языков |
| 🔓 **Полностью открытый** | Лицензия MIT, прозрачный и настраиваемый |

---

## 🆚 Почему Flux?

| | Flux | Другие клиенты |
|:---:|:---:|:---:|
| **Сложность настройки** | 🟢 Одна строка | 🔴 Требуется бэкенд |
| **Платформы** | 🟢 5 платформ | 🟡 Обычно 1-2 |
| **UI дизайн** | 🟢 Современный Material 3 | 🟡 Функциональность |
| **Протоколы** | 🟢 7+ протоколов | 🟡 Ограниченно |
| **Языки** | 🟢 16 языков | 🟡 Только EN/CN |
| **Open Source** | 🟢 100% открытый | 🔴 Закрытый/частично |
| **Брендинг** | 🟢 Лёгкий ребрендинг | 🔴 Изменение исходников |

---

## 📱 Скриншоты

### 📱 Мобильные

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 Десктоп

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 Кастомизация и коммерческая поддержка

Если вам нужно:
-   🔥 **Изменить название и логотип приложения**
-   🎨 **Кастомные UI темы**
-   🚀 **Добавить расширенные функции**

Свяжитесь в Telegram: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 Поддерживаемые протоколы

✅ **Проверено на Android и Windows**:
- **Hysteria2**: Быстрый протокол обхода блокировок
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 Быстрый старт

### 1. Клонирование репозитория

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. Настройка API URL (Важно)

Откройте `lib/services/api_config.dart` и измените:

```dart
Future<String> getBaseUrl() async {
  // Измените на URL вашей панели
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. Изменение App ID

Замените `com.example.yourapp` на ваш App ID:

| Платформа | Путь к файлу | Изменяемое поле |
|-----------|--------------|-----------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` и `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` в `msix_config` |

### 4. Замена иконки приложения

1. Подготовьте PNG изображение **1024x1024**
2. Поместите в `assets/images/app_icon.png`
3. Выполните:
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. Сборка

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

## ☕ Поддержать проект

Если этот проект помог вам, угостите автора кофе!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 Связанные проекты

### Ядра прокси
-   [Xray-core](https://github.com/XTLS/Xray-core): Основное ядро проекта
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): Классическое прокси-ядро
-   [Hysteria](https://github.com/apernet/hysteria): Мощный протокол обхода блокировок

### Панели управления
-   [V2Board](https://github.com/v2board/v2board): Мощная панель V2Ray

---

## 💬 Присоединяйтесь к сообществу

- **Telegram группа**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
