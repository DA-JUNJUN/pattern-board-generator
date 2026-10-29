# 通用图案板生成工具

将任意主题转化为具有商业审美、构成逻辑和统一画风的二维平面印花系列。项目跨主题使用，不预设节日、元素、配色或装饰；每个主题单独建立视觉 DNA 和构成方案。

当前仓库提供文档、项目级 Skill、官方画风参考、构成语法、正反案例与验收记录。它不是网页应用，不需要安装依赖。仓库中的 PDF 是导入的参考资料，不是本项目新生成的图案。

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
- [真实运行验收清单](evals/runtime-acceptance-checklist.md)

## 在 Codex 中调用 Skill

在仓库上下文中，推荐显式调用项目级 Skill：

```text
请使用 $pattern-board-generator：启动一个新的春季花卉图案板项目。
```

Skill 位于 `.agents/skills/pattern-board-generator/SKILL.md`。如果当前 Codex 会话没有发现该 Skill，应如实报告并停止依赖它执行；文件存在不等于新会话已经完成运行时加载。

## 上传参考图

在当前对话中直接附加图片或 PDF，并说明每份参考的职责，例如：

```text
图 1 只参考画风和笔触，不参考配色；
图 2 参考构成和疏密；
图 3 参考配色面积，不复制具体元素。
```

Codex 必须先确认文件实际可访问，再区分视觉观察、设计推断和待确认项。无法查看 PDF 页面图像时，应明确说明限制；文字摘要不能冒充视觉核对。参考资料用于提炼方法，不复制独特纹样、品牌、文字、水印或签名。

## 启动新主题

一个对话首次提出某个主题时，只进行简短建档：主题、核心元素与主辅建议、配色建议、构成建议，可附画风建议，并明确“本轮不生成图片”。即使首条消息包含“直接生成”，也不能跳过这一轮。

推荐首轮写法：

```text
请使用 $pattern-board-generator：新项目，冬季滑雪的小狗，计划制作六格图案板。先建档，本轮不生成图片。
```

每个新主题都要重新确定元素、配色、装饰、P 画风和 C 构成。通用二维印花规范可以复用，旧主题的具体设计变量不能自动继承。

## 授权生成

完成建档、参考分析、视觉 DNA 和图案板规划后，用户需在后续消息中明确授权当前输出。授权应包含主题或规划版本、输出类型、数量和关键限制，例如：

```text
基于已确认的“冬季滑雪小狗 v1”方案，授权生成一张 3×2 六格纯图案板；只生成这一张，不增加标题、色卡、产品或场景。
```

授权一次只覆盖指定的一张。新增板位、额外数量、重生成或扩大修改范围需要新的明确授权。只要求修改配色或画风时，已经确认的构成必须保持不变。

当前仓库没有执行过真实图像生成验收；静态检查、模拟测试、真实 Skill 调用和真实图像测试的状态见[真实运行验收清单](evals/runtime-acceptance-checklist.md)。

## 规则边界

通用规则规定方法与验收底线；主题档案独立决定元素、色彩、画法和构成参数。任何示例都不作为后续主题的默认风格。

2026-10-29 已导入一套原始规则包，其中包含 13 份 Markdown、4 页官方 P 画风 PDF 和 32 页正向案例 PDF。原始文件保留在 `references/source-materials/`；可执行提炼与原文分开维护。

独立的 P1–P4 PNG 原图、案例索引 CSV、编号 07 的质量美学标准、F01–F13 完整记录、F36 记录及 T29 回归用例仍然缺失。现有摘要和推断不能替代这些原件，详见[待补充资料](docs/missing-inputs.md)。
