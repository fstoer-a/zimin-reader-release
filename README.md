# 子皿文档阅读器（发布仓库）

本地 Markdown 文档阅读器 · Tauri 2 + WebView · Windows / Android

> 本仓库只发布安装包与更新清单，**不含源码**。源码仓库私有。

## 下载

到 [Releases](https://github.com/fstoer-a/zimin-reader-release/releases) 页下载对应平台的安装包：

| 平台 | 文件 |
|---|---|
| Windows x64 | `doc-reader_*_x64-setup.exe`（NSIS 安装包，支持应用内自动更新） |
| Android arm64 | `子皿文档阅读器_*_aarch64.apk` |

## 更新

- **Windows**：应用内「设置 → 关于 → 检查更新」，走本仓库 `latest.json`
- **Android**：应用内检查更新，下载 APK 后手动安装

## 数据目录

| 平台 | 位置 |
|---|---|
| Windows | exe 同级目录（便携）；不可写时回退 `%LOCALAPPDATA%\子皿文档阅读器` |
| Android | `/storage/emulated/0/子皿文档阅读器/`（需授予「所有文件访问」权限，应用内有引导） |

## 许可

© 2026 fstoer-a。保留所有权利。禁止未经授权的二次分发与修改再发布。
