# Engineering Playbook

面向人和编码 Agent 的工程流程资产库。这里维护三套长期规范：

| Profile | 解决的问题 | 入口 |
|---|---|---|
| Development | 一个新功能怎样从需求走到可交付 | [开发流程](profiles/development/README.md) |
| Refactoring | 一个结构性改造怎样保持行为、分期实施并安全收口 | [重构流程](profiles/refactoring/README.md) |
| Testing | 一个精确版本怎样完成测试、复测和发布准入 | [测试流程](profiles/testing/README.md) |

三套流程共享 [Core](core/README.md) 中的职责分离、分级、Gate、证据、独立复核和偏差协议。Profile 只描述各自不同的对象、状态和验收方式。

## 唯一事实源

- 本 Git 仓库是规范、模板和 Schema 的唯一可编辑源。
- 不与 Notion 或其他文档系统双写。
- 项目可以生成或复制规范快照，但必须标注采用的 Playbook 版本。
- 实际需求、方案、评审和测试记录留在业务项目中；本仓不保存 `cases/`。
- 项目专属环境、分支、命令、设备和资源限制留在项目自己的 `AGENTS.md` 或 `.playbook.yaml`，不写进通用 Profile。

## 使用方式

1. 先读 [Core](core/README.md)。
2. 按任务选择一个 Profile；开发中发生大规模结构调整时，可以同时启用 Development 和 Refactoring。
3. 从对应 `templates/` 复制所需文档到业务项目。
4. 用 `schemas/` 校验状态、档位和必填字段。
5. 全程以业务项目的 commit、diff 和落盘证据交接，不依赖聊天上下文。

## 规则优先级

```text
用户明确裁决 / 安全约束
  > Core 不变约束
  > Profile 专项规则
  > 项目适配规则
  > 单次任务方案
```

项目规则可以细化或收紧上层规则；需要放宽时必须记录为显式偏差并由用户裁决，不能静默覆盖。

## 目录

```text
core/                  三套流程共享的稳定规则
profiles/              development / refactoring / testing
templates/             可复制的空白文档骨架
schemas/               机器可读的字段、状态和档位定义
CONTRIBUTING.md         规范如何修改、评审和发布
SOURCES.md              初始迁移来源与基线
CHANGELOG.md            版本变化
VERSION                 当前版本
```

当前版本：[`0.1.0`](VERSION)。这是把三份现行规范迁入独立资产库后的首个基线版本。
