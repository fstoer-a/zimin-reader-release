# zimin-doc-reader 插件清单与文档

本仓库包含「子皿文档阅读器」的插件市场清单、发布安装包与开源文档（不含应用源码，源码仓库私有）。

- `plugins/manifest.json` — 插件市场清单（AI 审核插件，含 SHA-256 与下载地址）
- `docs/PLUGIN_REVIEW.md` — 插件审核标准与首批审核报告
- `docs/PLUGIN_MIRROR.md` — 镜像配置说明
- [Releases](https://github.com/fstoer-a/zimin-reader-release/releases) — 应用下载（Windows / Android）

## 镜像

应用内置镜像链（直连 + ghproxy + jsdelivr），全部指向本仓库 `plugins/manifest.json`。
自建镜像只需托管该文件，保持 URL 结构一致即可，详见 `docs/PLUGIN_MIRROR.md`。

## 许可

© 2026 fstoer-a。保留所有权利。插件清单与文档可引用，禁止未经授权的整体复制。
