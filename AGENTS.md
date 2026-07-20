# Engineering Playbook 维护规则

修改本仓前先阅读 `README.md`、`CONTRIBUTING.md` 和受影响的 `core/`、`profiles/` 文档。

- 本仓是开发、重构、测试三套规范的 Git 唯一事实源，不同步维护 Notion 副本。
- 不创建 `cases/` 或 `docs/`；实际任务记录留在业务项目。
- 三套流程共同且语义一致的规则进入 `core/`；专项规则进入对应 `profiles/`。
- 项目分支、环境、语言命令、设备和资源限制不得写入通用 Profile。
- 流程按职责而不是人员、Agent 产品或具体模型书写。
- 改动产物结构时同步 `templates/` 和 `schemas/`。
- 修改强制 Gate、状态或必填产物时更新 `VERSION`、`CHANGELOG.md`，并按破坏性变更处理。
- 提交前校验所有相对链接和 YAML，确认 `core/`、`profiles/`、`templates/`、`schemas/` 中没有项目专属地址或分支名。
