[English](README_EN.md) | 简体中文 | [繁體中文](docs/README_TW.md) | [日本語](docs/README_JA.md) | [한국어](docs/README_KO.md) | [Русский](docs/README_RU.md) | [हिन्दी](docs/README_HI.md) | [Español](docs/README_ES.md) | [Português](docs/README_PT.md) | [Français](docs/README_FR.md) | [Deutsch](docs/README_DE.md) | [العربية](docs/README_AR.md) | [Türkçe](docs/README_TR.md) | [Tiếng Việt](docs/README_VI.md) | [ไทย](docs/README_TH.md) | [Indonesia](docs/README_ID.md)

<div align="center">

# ⚡ Flux

### 给机场站长的专属客户端解决方案

**基于 Flutter 的跨平台代理客户端，专为 V2Board 机场运营者打造**

改一行 API 地址 → 编译 → 拥有专属品牌 App

[![Stars](https://img.shields.io/github/stars/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/stargazers)
[![Forks](https://img.shields.io/github/forks/flux-apphub/flux?style=flat-square&logo=github)](https://github.com/flux-apphub/flux/network/members)
[![License](https://img.shields.io/github/license/flux-apphub/flux?style=flat-square)](LICENSE)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter)](https://flutter.dev)

💬 [加入 Telegram 群组](https://t.me/+62Otr015kSs1YmNk) · 📞 [商务合作 @fluxdeveloper](https://t.me/fluxdeveloper)

</div>

---

## 🎯 Flux 是什么？

> **Flux 不是给普通用户用的 VPN 工具，而是给机场站长「造客户端」的开源方案。**

如果你正在运营 V2Board 面板，你一定遇到过这些问题：

- 😫 用户抱怨第三方客户端太丑、太复杂
- 😫 想出一个自己品牌的 App，但不会开发
- 😫 找外包太贵，找开源项目又不知道怎么改

**Flux 就是为了解决这些问题而生的。**

---

## 👥 Flux 适合谁用？

| 用户类型 | 你的需求 | Flux 能帮你 |
|:---:|:---|:---|
| 🛫 **机场站长** | 想快速出一个专属品牌客户端 | ✅ 改一行代码，5 分钟编译出 App |
| 🧑‍💻 **二次开发者** | 想 fork 一个干净的 Flutter 代理项目 | ✅ MIT 协议，可自由商用 |
| 👤 **终端用户** | 想要一个好看、好用的代理工具 | ✅ 联系你的机场获取专属客户端 |

---

## 🆚 为什么选 Flux？（对比竞品）

| 特性 | Flux | v2rayNG | Clash | Shadowrocket |
|:---|:---:|:---:|:---:|:---:|
| **跨平台** | ✅ 5 端 | ❌ 仅 Android | ⚠️ 多客户端 | ❌ 仅 iOS |
| **V2Board API 原生支持** | ✅ 内置 | ❌ 需手动导入 | ❌ 需手动导入 | ❌ 需手动导入 |
| **Flutter 现代 UI** | ✅ Material 3 | ❌ 原生安卓 | ❌ Web 风格 | ❌ 原生 iOS |
| **白标定制（换名换图标）** | ✅ 开箱即用 | ❌ 需改源码 | ❌ 困难 | ❌ 不可能 |
| **可商用** | ✅ MIT 协议 | ✅ | ⚠️ | ❌ |
| **开源** | ✅ 100% | ✅ | ⚠️ 部分 | ❌ |

**👉 简单说：Flux 是目前唯一一个「开箱即用、可白标、可商用」的 V2Board 客户端方案。**

---

## ⚡ 5 分钟快速上手

```bash
# 1. 克隆项目
git clone https://github.com/flux-apphub/flux.git
cd flux

# 2. 安装依赖
flutter pub get

# 3. 改一行代码（把你的面板地址填进去）
# 打开 lib/services/api_config.dart，修改：
# return 'https://你的面板.com/api/v1';

# 4. 运行
flutter run
```

**Done. 你的专属 V2Board 客户端已经跑起来了。**

---

## 📱 界面预览

<details>
<summary>📱 点击查看手机端截图</summary>

| | | |
| :---: | :---: | :---: |
| <img src="assets/images/screenshots/1.png" width="200"> | <img src="assets/images/screenshots/2.png" width="200"> | <img src="assets/images/screenshots/3.png" width="200"> |
| <img src="assets/images/screenshots/4.png" width="200"> | <img src="assets/images/screenshots/5.png" width="200"> | |

</details>

<details>
<summary>💻 点击查看桌面端截图</summary>

| | |
| :---: | :---: |
| <img src="assets/images/screenshots/6.png" width="400"> | <img src="assets/images/screenshots/7.png" width="400"> |
| <img src="assets/images/screenshots/8.png" width="400"> | <img src="assets/images/screenshots/9.png" width="400"> |

</details>

---

## 🛠 支持的协议

| 协议 | 状态 | 说明 |
|:---|:---:|:---|
| **Hysteria2** | ✅ 已验证 | 极速抗封锁 |
| **VLESS Reality** | ✅ 已验证 | 最新防检测技术 |
| **VMess** | ✅ 已验证 | TCP / WebSocket |
| **Trojan** | ✅ 已验证 | - |
| **Shadowsocks** | ✅ 已验证 | AEAD 加密 |

> ⚠️ iOS/macOS 版本尚未完整测试（开发者没有苹果设备），欢迎社区贡献！

---

## 🎨 定制指南（给站长）

### 改名换图标只需 3 步：

**第一步：改 App ID（包名）**

| 平台 | 文件 | 改什么 |
|:---|:---|:---|
| Android | `android/app/build.gradle.kts` | `applicationId` |
| iOS | `ios/Runner.xcodeproj/project.pbxproj` | `PRODUCT_BUNDLE_IDENTIFIER` |
| macOS | `macos/Runner/Configs/AppInfo.xcconfig` | `PRODUCT_BUNDLE_IDENTIFIER` |
| Windows | `pubspec.yaml` | `msix_config.identity_name` |
| Linux | `linux/CMakeLists.txt` | `APPLICATION_ID` |

**第二步：改 App 名称**

| 平台 | 文件 | 改什么 |
|:---|:---|:---|
| Android | `AndroidManifest.xml` | `android:label` |
| iOS | `Info.plist` | `CFBundleDisplayName` |
| Windows | `Runner.rc` | `ProductName` |

**第三步：换图标**

```bash
# 把 1024x1024 的 PNG 图标放到 assets/images/app_icon.png
flutter pub run flutter_launcher_icons
```

**完成。你已经拥有了一个专属品牌的代理客户端。**

---

## 💰 商业合作

如果你需要：

| 服务 | 说明 |
|:---|:---|
| 🔥 **快速出包** | 帮你编译好 Android/iOS/Windows 安装包 |
| 🎨 **UI 定制** | 改配色、改布局、加功能 |
| 🔐 **授权系统** | 加入设备授权、到期提醒等 |

**联系方式：** [@fluxdeveloper](https://t.me/fluxdeveloper)

---

## 🔧 技术架构（给开发者）

<details>
<summary>点击展开技术细节</summary>

### 核心架构

- **UI 层**: Flutter 3.x + Material Design 3
- **逻辑层**: `UnifiedVpnService` 统一调度
- **内核层**: V2Ray / Xray Core

### 各平台实现

| 平台 | 机制 | 说明 |
|:---|:---|:---|
| Android | `VpnService` API | TUN 模式，无需 Root |
| iOS | `NetworkExtension` | Packet Tunnel Provider |
| Desktop | System Proxy + Sidecar | 系统代理 + 内核进程 |

### 项目结构

```
lib/
├── main.dart          # 入口
├── screens/           # 页面
├── services/          # 核心服务
│   ├── api_config.dart    # 👈 改这里！
│   ├── v2ray_service.dart
│   └── vpn_service.dart
├── models/            # 数据模型
└── widgets/           # 组件
```

</details>

---

## 🌐 OSS 远程配置（高级功能）

<details>
<summary>点击展开 OSS 配置说明</summary>

Flux 支持通过 OSS/CDN 下发配置，实现：
- 域名自动切换
- 版本更新通知
- 公告推送

配置 `lib/services/remote_config_service.dart` 中的 `_ossUrls`，上传 JSON 到你的 OSS。

</details>

---

## 🔗 相关项目

- [Xray-core](https://github.com/XTLS/Xray-core) - 核心引擎
- [V2Board](https://github.com/v2board/v2board) - 机场面板
- [hev-socks5-tunnel](https://github.com/heiher/hev-socks5-tunnel) - 高性能 SOCKS5 隧道

---

## ☕ 赞助

如果 Flux 帮你省了开发费用，欢迎请作者喝杯咖啡：

| USDT (TRC20) | USDC (Arbitrum) | ETH (Arbitrum) |
| :---: | :---: | :---: |
| <img src="assets/images/donation/usdt_trc20.png" width="150"> | <img src="assets/images/donation/usdc_arbitrum.png" width="150"> | <img src="assets/images/donation/eth_arbitrum.png" width="150"> |

---

## 📄 License

MIT License - 可自由使用、修改、分发和商用。

---

<div align="center">

**Flux** - 给机场站长的专属客户端方案

*关键词：V2Board客户端、机场专属App、Flutter代理客户端、白标VPN、开源代理工具*

</div>
