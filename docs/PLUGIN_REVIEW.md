# 插件审核报告（0.9.0 首批）

审核时间：2026-11-15
审核工具：tools/_plugin_audit_raw.json（元数据体检 + 源码扫描）
候选池：npm 关键词 markdown-it 下载量与知名度 TOP 30，过滤明显不适配阅读器场景后取 20 个

## 审核标准（摘要）

1. 维护者可信（原作者/知名组织）或包历史 ≥ 3 年
2. 源码扫描零命中：child_process / fs / eval / new Function / 网络调用（命中仅在测试文件时豁免）
3. 无未审核的传递依赖
4. 渲染快照双端一致（上架前人工跑 tools/render_snapshot.py）
5. 不允许触碰 window / document（除渲染产物注入）

## 审核结果

| 插件 | 版本 | SHA-256（前16） | 扫描 | 结论 |
|---|---|---|---|---|
| markdown-it-emoji | 3.1.0 | 9ce648b8d484edfb… | 0 命中 | ✅ 通过 |
| markdown-it-mark | 4.0.0 | 9705e91a79a18240… | 0 命中 | ✅ 通过 |
| markdown-it-ins | 4.0.0 | bf7cbf37d3aa0534… | 0 命中 | ✅ 通过 |
| markdown-it-sub | 2.0.0 | 81e60321b6e42bb3… | 0 命中 | ✅ 通过 |
| markdown-it-sup | 2.0.0 | 03f5a7a8129fed41… | 0 命中 | ✅ 通过 |
| markdown-it-attrs | 5.0.1 | 7473022b896a8762… | 0 命中 | ✅ 通过 |
| markdown-it-container | 4.0.0 | d5bd78dd73d50aee… | 0 命中 | ✅ 通过 |
| markdown-it-abbr | 2.0.0 | 61d4b33f587eeeac… | 0 命中 | ✅ 通过 |
| markdown-it-deflist | 4.0.0 | eb70f804a1619fe9… | 0 命中 | ✅ 通过 |
| markdown-it-anchor | 10.1.0 | 4576a1f8bca5f20d… | 0 命中 | ✅ 通过 |
| markdown-it-table-of-contents | 1.3.0 | a16855a5bdd8e795… | 0 命中 | ✅ 通过 |
| markdown-it-link-attributes | 4.0.1 | 7ee2ee700ad806be… | 0 命中 | ✅ 通过 |
| markdown-it-image-figures | 2.1.1 | 03f3dc40e6f75833… | 0 命中 | ✅ 通过 |
| markdown-it-github-alerts | 1.0.1 | 14e3314c7092c981… | 0 命中 | ✅ 通过 |
| markdown-it-cjk-friendly | 3.0.0 | 4b9f27ab17f23bb5… | 0 命中 | ✅ 通过 |
| @vscode/markdown-it-katex | 1.1.2 | 763ae1c76cda85d2… | 0 命中 | ✅ 通过 |
| markdown-it-texmath | 1.0.0 | afca1f328047ecd9… | 1 命中（测试文件，豁免） | ✅ 通过 |
| markdown-it-dollarmath | 0.5.0 | 226d138dc84291af… | 0 命中 | ✅ 通过 |
| markdown-it-task-checkbox | 1.0.6 | 326007dea61d28f7… | 1 命中（测试文件，豁免） | ✅ 通过 |
| markdown-it-table | 5.0.0 | 01d40f23f8f13285… | 0 命中 | ✅ 通过 |

## 复审触发条件

- npm 包 maintainer 变更 / 发布新版 → 自动重审
- 每季度全量复审一次
- 重审不过 → 清单下架；已装版本提示「已下架，可继续用或卸载」
