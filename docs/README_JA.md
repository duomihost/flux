[English](../README_EN.md) | [简体中文](../README.md) | [繁體中文](README_TW.md) | 日本語 | [한국어](README_KO.md) | [Русский](README_RU.md) | [हिन्दी](README_HI.md) | [Español](README_ES.md) | [Português](README_PT.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [العربية](README_AR.md) | [Türkçe](README_TR.md) | [Tiếng Việt](README_VI.md) | [ไทย](README_TH.md) | [Indonesia](README_ID.md)

<div align="center">

# ⚡ Flux

**🚀 V2Board 向けに設計されたオープンソースのクロスプラットフォームプロキシクライアント**

*1行で設定完了 · Flutter で5プラットフォーム対応 · 16言語サポート*

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS%20%7C%20Linux-333?style=flat-square)](#)

---

**Flux** は [V2Board](https://github.com/v2board/v2board) 向けに設計された最新のクライアントです。  
**1行の API アドレス変更**だけで、あなただけのブランドアプリを手に入れましょう。

</div>

---

## ✨ 主な特徴

| 特徴 | 説明 |
|:---:|:---|
| ⚡ **即時セットアップ** | API URL を1行変更するだけ、バックエンド開発不要 |
| 🎨 **美しい UI** | Material Design 3、ダーク/ライトテーマ対応 |
| 📱 **クロスプラットフォーム** | Flutter で Android / iOS / Windows / macOS / Linux に対応 |
| 🔐 **マルチプロトコル** | Hysteria2 / VLESS Reality / VMess / Trojan / Shadowsocks / WireGuard / TUIC |
| 🌍 **グローバル対応** | 16言語対応 |
| 🔓 **完全オープンソース** | MIT ライセンス、透明で自由にカスタマイズ可能 |

---

## 🆚 なぜ Flux を選ぶべきか？

| | Flux | 他のクライアント |
|:---:|:---:|:---:|
| **セットアップ難易度** | 🟢 1行変更 | 🔴 バックエンド必要 |
| **プラットフォーム** | 🟢 5プラットフォーム統一 | 🟡 通常1-2 |
| **UI デザイン** | 🟢 モダン Material 3 | 🟡 機能優先 |
| **プロトコル対応** | 🟢 7+ 対応 | 🟡 限定的 |
| **多言語** | 🟢 16言語 | 🟡 英中のみ |
| **オープンソース** | 🟢 100% オープン | 🔴 クローズド/部分的 |
| **ブランディング** | 🟢 簡単リブランド | 🔴 ソース変更必要 |

---

## 📱 スクリーンショット

### 📱 モバイル

| | | |
| :---: | :---: | :---: |
| <img src="../assets/images/screenshots/1.png" width="200"> | <img src="../assets/images/screenshots/2.png" width="200"> | <img src="../assets/images/screenshots/3.png" width="200"> |
| <img src="../assets/images/screenshots/4.png" width="200"> | <img src="../assets/images/screenshots/5.png" width="200"> | |

### 💻 デスクトップ

| | |
| :---: | :---: |
| <img src="../assets/images/screenshots/6.png" width="400"> | <img src="../assets/images/screenshots/7.png" width="400"> |
| <img src="../assets/images/screenshots/8.png" width="400"> | <img src="../assets/images/screenshots/9.png" width="400"> |

---

## 📞 カスタマイズ & 商用サポート

以下のサービスが必要な場合：
-   🔥 **アプリ名とロゴの変更**
-   🎨 **カスタム UI テーマ**
-   🚀 **高度な機能の追加**

Telegram でお問い合わせ：👉 **[@fluxdeveloper](https://t.me/fluxdeveloper)**

---

## 🛠 サポートされているプロトコル

✅ **検証済みプラットフォーム (Android & Windows)**:
- **Hysteria2**: 高速な検閲回避プロトコル
- **VLESS** (Vision / Reality)
- **VMess** (TCP / WebSocket)
- **Trojan**
- **Shadowsocks** (AEAD)
- **WireGuard**
- **TUIC**

---

## 🚀 クイックスタート

### 1. リポジトリのクローン

```bash
git clone https://github.com/flux-apphub/flux.git
cd flux
```

### 2. API URL の設定 (重要)

`lib/services/api_config.dart` を開いて変更：

```dart
Future<String> getBaseUrl() async {
  // パネルの URL に変更
  return 'https://your-panel-domain.com/api/v1'; 
}
```

### 3. アプリ ID の変更

`com.example.yourapp` を自分の App ID に置き換え：

| プラットフォーム | ファイルパス | 変更項目 |
|-----------------|-------------|----------|
| **Android** | `android/app/build.gradle.kts` | `applicationId` と `namespace` |
| **iOS** | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **macOS** | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| **Linux** | `linux/CMakeLists.txt` | `APPLICATION_ID` |
| **Windows** | `pubspec.yaml` | `msix_config` の `identity_name` |

### 4. アプリアイコンの置き換え

1. **1024x1024** の PNG 画像を準備
2. `assets/images/app_icon.png` に配置
3. 実行：
   ```bash
   flutter pub run flutter_launcher_icons
   ```

### 5. ビルド

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

## ☕ プロジェクトを支援

このプロジェクトが役立った場合は、著者にコーヒーを一杯奢ってください！

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) | USDT (ERC20) |
| :---: | :---: | :---: | :---: |
| <img src="../assets/images/donation/usdt_trc20.png" width="180" alt="USDT TRC20"> | <img src="../assets/images/donation/usdc_arbitrum.png" width="180" alt="USDC Arbitrum"> | <img src="../assets/images/donation/eth_arbitrum.png" width="180" alt="ETH Arbitrum"> | <img src="../assets/images/donation/usdt_erc20.png" width="180" alt="USDT ERC20"> |

---

## 🔗 関連プロジェクト

### コアプロキシエンジン
-   [Xray-core](https://github.com/XTLS/Xray-core): このプロジェクトで使用されているコアエンジン
-   [V2Ray-core](https://github.com/v2fly/v2ray-core): クラシックなプロキシコア
-   [Hysteria](https://github.com/apernet/hysteria): 強力な検閲回避プロトコル

### パネル & 管理
-   [V2Board](https://github.com/v2board/v2board): 強力な V2Ray パネル

---

## 💬 コミュニティに参加

- **Telegram グループ**: [https://t.me/+62Otr015kSs1YmNk](https://t.me/+62Otr015kSs1YmNk)

---

<div align="center">

**Flux Open Source** - Make Connection Simple.

</div>
