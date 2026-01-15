[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | [日本語](README_JA.md) | 한국어 | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 V2Board를 위한 오픈 소스 크로스 플랫폼 프록시 클라이언트**

*한 줄 설정 · Flutter 5개 플랫폼 통합 · 16개 언어 지원*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

💬 **커뮤니티 참여**: [텔레그램 그룹](https://t.me/+62Otr015kSs1YmNk) · 📞 **비즈니스**: [@fluxdeveloper](https://t.me/fluxdeveloper)

---

**Flux**는 [V2Board](https://github.com/v2board/v2board)를 위해 설계된 현대적인 클라이언트입니다.  
**API 주소 한 줄만 수정**하면 나만의 브랜드 앱을 가질 수 있습니다.

</div>

---

## ✨ 주요 기능

| 기능 | 설명 |
|:---:|:---|
| ⚡ **즉시 설정** | API URL 한 줄만 수정, 백엔드 개발 필요 없음 |
| 🎨 **아름다운 UI** | Material Design 3, 다크/라이트 테마 지원 |
| 📱 **크로스 플랫폼** | Flutter로 Android / iOS / Windows / macOS / Linux 지원 |
| 🔐 **다중 프로토콜** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **글로벌 지원** | 16개 언어 지원 |
| 🔓 **완전 오픈 소스** | MIT 라이선스, 투명하고 자유롭게 커스터마이징 가능 |

---

## 🆚 왜 Flux를 선택해야 하나요?

| | Flux | 다른 클라이언트 |
|:---:|:---:|:---:|
| **설정 난이도** | 🟢 한 줄 변경 | 🔴 백엔드 필요 |
| **플랫폼 지원** | 🟢 5개 플랫폼 통합 | 🟡 보통 1-2개 |
| **UI 디자인** | 🟢 모던 Material 3 | 🟡 기능 우선 |
| **프로토콜 지원** | 🟢 7+ 프로토콜 | 🟡 제한적 |
| **다국어** | 🟢 16개 언어 | 🟡 영/중만 |
| **오픈 소스** | 🟢 100% 오픈 | 🔴 클로즈드/부분적 |
| **브랜딩** | 🟢 쉬운 리브랜드 | 🔴 소스 수정 필요 |

---

## 📱 스크린샷

### 📱 모바일

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 데스크톱

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 커스터마이징 & 상업적 지원

필요하신 경우:
-   🔥 **앱 이름 및 로고 변경**
-   🎨 **커스텀 UI 테마**
-   🚀 **고급 기능 추가**

텔레그램으로 연락: 👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 지원 프로토콜

✅ **검증된 플랫폼 (Android & Windows)**:
- **Hysteria2**: 빠른 검열 우회 프로토콜
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 빠른 시작

### 1. 저장소 클론

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. API URL 설정 (필수)

`lib/services/api_config.dart`를 열어 수정:

```dart
Future<String> getBaseUrl() async {
  // 패널 URL로 변경
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. 앱 ID 변경

`com.example.yourapp`을 자신의 App ID로 교체:

| 플랫폼 | 파일 경로 | 변경 항목 |
|--------|-----------|----------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` 및 `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `msix_config`의 `identity_name` |

### 4. 앱 아이콘 교체

1. **1024x1024** PNG 이미지 준비
2. `assets/images/app_icon.png`에 배치
3. 실행:
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. 빌드

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

## ☕ 프로젝트 후원

이 프로젝트가 도움이 되었다면, 개발자에게 커피 한 잔을 후원해주세요!

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 관련 프로젝트

### 코어 프록시 엔진
-   [Xray-core](https://github.com/XTLS/Xray-core): 이 프로젝트에서 사용하는 코어 엔진
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): 클래식 프록시 코어
-   [Hysteria](https://github.com/apernet/hysteria): 강력한 검열 우회 프로토콜

### 패널 & 관리
-   [V2Board](https://github.com/v2board/v2board): 강력한 V2Ray 패널

---

## 💬 커뮤니티 참여

- **텔레그램 그룹**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
