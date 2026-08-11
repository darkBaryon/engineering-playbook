# Changelog

本项目使用语义化版本：

- Patch：措辞、链接、错别字或不改变流程行为的修订；
- Minor：新增向后兼容的可选规则、模板或字段；
- Major：改变强制 Gate、状态流转、职责边界或必需产物。

## 1.1.0 - 2026-08-12

- 新增 Change 模型（`change/`）：Change 作为工程账本的最小完整单元，开发、重构、测试降级为其内部流程类型；现有三套规范原文不变；
- 新增风险分级与条件 Gate：L1/L2/L3 按风险定流程重量，Gate 1 仅在存在拍板项时触发，无拍板项自动继续并留痕；Gate 2 不可省略但重量分级；
- 新增收敛评审：实施后评估系统整体健康度（重复 / 膨胀 / 边界 / 契约 / 测试 / 非功能），出口为无碍 / Blocking / REF Case / Finding；第一原则为"机械检查产事实，判断只属于评审 agent，指标不得直接构成结论"；
- 新增 Finding 台账：记录看到但暂不修的结构问题，含豁免机制与转化触发条件（`convert_when`）；
- 新增 Change 收尾的知识沉淀清单：过程记录留 Workbench，长期事实迁移到主仓库文档（测试 / OpenAPI / ADR / Runbook / AGENTS.md）；
- 新增 `templates/change/convergence-review.md` 与 `skills/convergence-review/`（skill 参考实现）。

## 1.0.0 - 2026-07-21

- 将开发、重构、测试改为三套分别自包含的执行手册；
- 按实际执行顺序拆分编号章节，入口页提供完整流程和最小清单；
- 删除需要跨流程拼装阅读的 `core/` 与 `profiles/` 结构；
- 增加 `MAINTENANCE.md`，通过一致性表维护三套规范的共同纪律；
- 删除没有程序消费的 `schemas/` 和示意 checklist YAML；
- 保留真正用于复制的记录模板，并移除模板中的 Profile 阅读术语；
- 明确共享模拟器等资源只在实际操作窗口占用，具体协议由业务项目定义。

## 0.1.0 - 2026-07-20

- 建立 Development、Refactoring、Testing 三个 Profile；
- 从三份现行规范抽取 Core：职责、分级、Gate、证据、评审和偏差协议；
- 移除 Notion 双写和具体模型绑定；
- 将项目专属分支、环境、语言工具链和模拟器规则移出通用规范；
- 增加三套流程的模板与机器可读 Schema；
- 明确本仓不保存实际案例记录。
