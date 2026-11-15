# 插件市场镜像配置

插件市场清单与插件包默认从以下地址加载（按顺序尝试）：

1. `https://raw.githubusercontent.com/fstoer-a/zimin-doc-reader/main/plugins/manifest.json`
2. `https://ghproxy.net/https://raw.githubusercontent.com/fstoer-a/zimin-doc-reader/main/plugins/manifest.json`（GitHub 镜像）

## 自定义镜像

在数据目录（exe 同级 / 安卓 `/storage/emulated/0/子皿文档阅读器/`）创建 `config.json`：

```json
{
  "pluginMirror": "https://你的镜像地址/路径"
}
```

配置后插件市场只从该地址加载清单（`<镜像>/manifest.json`），
插件包下载地址以清单内 `download` 字段为准（审核时已写入直链）。

## 安全说明

- 所有市场插件包都经过 AI 审核（源码扫描 + SHA-256 校验）
- 安装时校验 SHA-256，不匹配即拒绝
- 镜像站只加速清单/包下载，**审核报告与签名哈希以 GitHub 原仓库为准**
- 详见 docs/PLUGIN_REVIEW.md
