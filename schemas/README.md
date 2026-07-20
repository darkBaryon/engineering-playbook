# Schema

这些 YAML 定义三套 Profile 的最小机器可读契约，用于校验业务项目中的任务记录。它们不是项目配置，也不包含具体命令或环境。

- [`common.yaml`](common.yaml)：共同字段和结论；
- [`development.yaml`](development.yaml)：开发档位、状态、产物和 Gate；
- [`refactoring.yaml`](refactoring.yaml)：重构档位、状态、产物和 Gate；
- [`testing.yaml`](testing.yaml)：测试档位、状态、用例结论和 Gate。

Schema 修改必须同步对应 Profile 与模板。删除状态、Gate 或必填产物属于破坏性变更。
