[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | العربية | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div dir="rtl" align="center">

# ⚡ Flux

**🚀 عميل بروكسي مفتوح المصدر متعدد المنصات لـ V2Board**

*إعداد بسطر واحد · Flutter لـ 5 منصات · 16 لغة*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

💬 **انضم إلى المجتمع**: [مجموعة تيليجرام](https://t.me/+62Otr015kSs1YmNk) · 📞 **للأعمال**: [@fluxdeveloper](https://t.me/fluxdeveloper)

---

**Flux** هو العميل الحديث المصمم لـ [V2Board](https://github.com/v2board/v2board).  
احصل على تطبيقك بعلامتك التجارية بتغيير **سطر واحد فقط**.

</div>

---

## ✨ الميزات الرئيسية

| الميزة | الوصف |
|:---:|:---|
| ⚡ **إعداد فوري** | عدّل رابط API واحد فقط، لا حاجة لتطوير الخادم |
| 🎨 **واجهة جميلة** | Material Design 3، دعم الوضع الداكن/الفاتح |
| 📱 **متعدد المنصات** | Flutter لـ Android / iOS / Windows / macOS / Linux |
| 🔐 **بروتوكولات متعددة** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **دعم عالمي** | 16 لغة |
| 🔓 **مفتوح المصدر بالكامل** | رخصة MIT، شفاف وقابل للتخصيص |

---

## 🆚 لماذا Flux؟

| | Flux | عملاء آخرون |
|:---:|:---:|:---:|
| **صعوبة الإعداد** | 🟢 سطر واحد | 🔴 خادم مطلوب |
| **المنصات** | 🟢 5 موحدة | 🟡 عادة 1-2 |
| **تصميم UI** | 🟢 Material 3 حديث | 🟡 الوظيفة أولاً |
| **البروتوكولات** | 🟢 7+ بروتوكول | 🟡 محدود |
| **اللغات** | 🟢 16 لغة | 🟡 EN/CN فقط |
| **مفتوح المصدر** | 🟢 100% مفتوح | 🔴 مغلق/جزئي |
| **العلامة التجارية** | 🟢 إعادة العلامة سهلة | 🔴 تعديل الكود |

---

## 📱 لقطات الشاشة

### 📱 الجوال

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 سطح المكتب

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 التخصيص والدعم التجاري

إذا كنت بحاجة إلى:
-   🔥 **تغيير اسم التطبيق والشعار**
-   🎨 **سمات UI مخصصة**
-   🚀 **إضافة ميزات متقدمة**

تواصل على تيليجرام: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 البروتوكولات المدعومة

✅ **تم التحقق على Android و Windows**:
- **Hysteria2**: بروتوكول سريع لتجاوز الحجب
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 البداية السريعة

### 1. استنساخ المستودع

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. تكوين رابط API (أساسي)

افتح `lib/services/api_config.dart` وعدّل:

```dart
Future<String> getBaseUrl() async {
  // غيّر إلى رابط لوحتك
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. تغيير App ID

استبدل `com.example.yourapp` بـ App ID الخاص بك:

| المنصة | مسار الملف | الحقل للتعديل |
|--------|-----------|---------------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` و `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `identity_name` في `msix_config` |

### 4. استبدال أيقونة التطبيق

1. جهّز صورة PNG **1024x1024**
2. ضعها في `assets/images/app_icon.png`
3. نفّذ:
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. البناء

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

## ☕ ادعم المشروع

إذا ساعدك هذا المشروع، قدّم قهوة للمؤلف!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 مشاريع ذات صلة

### محركات البروكسي
-   [Xray-core](https://github.com/XTLS/Xray-core): المحرك الأساسي لهذا المشروع
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): نواة بروكسي كلاسيكية
-   [Hysteria](https://github.com/apernet/hysteria): بروتوكول قوي لتجاوز الحجب

### اللوحات والإدارة
-   [V2Board](https://github.com/v2board/v2board): لوحة V2Ray قوية

---

## 💬 انضم إلى المجتمع

- **مجموعة تيليجرام**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
