# 初始来源

`0.1.0` 由以下三份已在真实任务中使用过的规范整理而来。迁移不是逐字复制：共性进入 `core/`，流程差异进入 `profiles/`，项目专属约束留在原项目。

| 规范 | 原始位置 | 基线 commit | 迁移说明 |
|---|---|---|---|
| 开发流程 | [`darkBaryon/xhs-recon/workbench`](https://github.com/darkBaryon/xhs-recon/tree/main/workbench) | `1c0ad324444f9b7d3b3378130c6d415fa290d145` | 保留需求、方案、评审、实施、并行开发骨架；移除 xhs-recon 专属目录和命令 |
| 重构流程 | `house-manager/shared-docs/backend/refactoring.md` 及子文档 | `da9054f2c2d04921f9b7ed62519f741ea3b5fefa` | Git 版本成为迁移来源；移除 Notion 双写、Go/wire/sit 等项目绑定 |
| 测试流程 | `zxw_app` 分支 `feat_2607_test_process_standard` | `c1b32724a650f0bf82b6101f880dc5827a5871e3` | 保留完整测试与复测流程；移除 Flutter、开发地址、模拟器锁和 sit 规则 |

后续修改只发生在本仓，不再从这些来源反向同步。
