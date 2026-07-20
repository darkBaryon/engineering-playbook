# 初始来源

本仓最初由三份已经在真实任务中使用过的规范迁移而来：

| 规范 | 原始位置 | 基线 commit | 保留的核心经验 |
|---|---|---|---|
| 开发 | [`darkBaryon/xhs-recon/workbench`](https://github.com/darkBaryon/xhs-recon/tree/main/workbench) | `1c0ad324444f9b7d3b3378130c6d415fa290d145` | 需求、方案、评审、实施、并行开发和双 Gate |
| 重构 | `house-manager/shared-docs/backend/refactoring.md` 及子文档 | `da9054f2c2d04921f9b7ed62519f741ea3b5fefa` | 行为基线、调用方盘点、接口白名单、分期迁移和阶段终扫 |
| 测试 | `zxw_app` 分支 `feat_2607_test_process_standard` | `c1b32724a650f0bf82b6101f880dc5827a5871e3` | 精确测试对象、分层执行、证据、缺陷复测和发布准入 |

`0.1.0` 曾将共性抽取为 `core/`，再把差异放进 `profiles/`。实践复核发现这种横向抽象增加了阅读和拼装成本，因此 `1.0.0` 恢复为三套按执行顺序组织、自包含的规范。

迁移不是逐字复制：真实项目的目录、命令、分支、环境、设备和资源限制仍留在业务项目。本仓不保存原项目案例，也不再从来源反向同步；后续修改只发生在本仓。
