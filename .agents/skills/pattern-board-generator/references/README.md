# 参考资料导航

此目录存放 Skill 的提炼规则与原始资料。具体主题的参考图、配色和设计卡应存入独立主题档案，不混入通用规则。

- [规则分层与主题变量](rule-model.md)
- [官方 P 画风定义与视觉核对](official-styles.md)
- [C1–C10 构成语法](composition-grammar.md)
- [正向案例、失败案例与经验状态](case-guidance.md)
- [原始资料清单与检查状态](source-materials-inventory.md)
- [原始资料目录](source-materials/)
- [通用流程](../../../../docs/design-workflow.md)
- [视觉 DNA](../../../../docs/visual-dna.md)
- [构图规则](../../../../docs/composition-rules.md)
- [质量验收](../../../../docs/quality-acceptance.md)
- [资料缺口](../../../../docs/missing-inputs.md)
- [主题档案模板](theme-template.md)

通用规范由仓库 `docs/` 维护，避免在参考目录重复保存产生版本分歧。

## 规则所有权

| 位置 | 职责 |
| --- | --- |
| `AGENTS.md` | 项目级硬边界：新主题闸门、授权、输出和证据要求 |
| `SKILL.md` | Codex 执行流程和停止条件 |
| `docs/` | 面向使用者的流程、设计与质量说明 |
| `references/` | 官方 P/C 定义、案例边界、原始资料和缺失记录 |
| `evals/` | 测试方案与证据，不反向创建新规则 |

相同硬边界可在 `AGENTS.md` 和 `SKILL.md` 重申以防越权；定义性细节只在对应 references 文件维护。若文字出现冲突，先遵循当前用户要求和 `AGENTS.md`，再修正文档漂移，不用 eval 结果覆盖正式规则。
