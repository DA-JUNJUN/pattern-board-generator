# 通用图案板生成工具

将任意主题转化为具有商业审美、构成逻辑和统一画风的二维平面印花系列。项目跨主题使用，不预设节日、元素、配色或装饰；每个主题单独建立视觉 DNA 和构成方案。

当前仓库提供文档、项目级 Skill、官方画风参考、构成语法、正反案例与验收记录。它不是网页应用，不需要安装依赖，也不包含本轮新生成的图片。

## 文件导航

- [项目协作规范](AGENTS.md)
- [通用设计流程](docs/design-workflow.md)
- [视觉 DNA](docs/visual-dna.md)
- [构图规则](docs/composition-rules.md)
- [质量验收标准](docs/quality-acceptance.md)
- [待补充资料](docs/missing-inputs.md)
- [通用图案板生成 Skill](.agents/skills/pattern-board-generator/SKILL.md)
- [规则分层与变量](.agents/skills/pattern-board-generator/references/rule-model.md)
- [官方画风定义](.agents/skills/pattern-board-generator/references/official-styles.md)
- [C1–C10 构成语法](.agents/skills/pattern-board-generator/references/composition-grammar.md)
- [正反案例与经验状态](.agents/skills/pattern-board-generator/references/case-guidance.md)
- [原始资料检查清单](.agents/skills/pattern-board-generator/references/source-materials-inventory.md)
- [测试用例和结果](evals/README.md)

## 使用方式

在 Codex 中调用 `pattern-board-generator` Skill。一个对话中的新主题首轮只完成简短建档，不生成图片；后续完成参考分析、视觉 DNA、图案板规划和当前输出的明确授权后，才可调用图像工具。

通用规则规定方法与验收底线；主题档案独立决定元素、色彩、画法和构成参数。任何示例都不作为后续主题的默认风格。

2026-10-29 已导入一套原始规则包，其中包含 13 份 Markdown、4 页官方 P 画风 PDF 和 32 页正向案例 PDF。原始文件保留在 `references/source-materials/`；可执行提炼与原文分开维护。
