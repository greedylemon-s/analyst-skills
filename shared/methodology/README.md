# shared/methodology — 跨 skill 通用方法论

所有 `analyst-*` skill 必须遵守。改这里 = 改所有分析师的"操作系统"。

| 文件 | 内容 | 是什么级别的约束 |
|---|---|---|
| [00-ironclad-rules.md](00-ironclad-rules.md) | 四大铁律：选框架 / 三源验证 / 信心等级 / 信息缺口透明 | 硬约束，违反 = 不合格 |
| [01-five-capabilities.md](01-five-capabilities.md) | 五种核心分析能力：追溯 / 第一性 / 纵向 / 横向 / 历史时间轴 | 硬约束，每次输出都要看得见痕迹 |
| [02-plain-speak.md](02-plain-speak.md) | 双层表达原则：大白话 + 专业版并存 | 硬约束，输出层 |
| [03-handoff-hints.md](03-handoff-hints.md) | 三人协作规范：tech → business / media 的指方向模板 | 硬约束，每次输出必备结尾 |
| [05-fact-exhaustion-before-inference.md](05-fact-exhaustion-before-inference.md) | 铁律 5：事实层穷尽到 bar 才能进推理层 | 硬约束，工作流先后顺序 |
| [06-buy-side-sell-side-lens.md](06-buy-side-sell-side-lens.md) | 买方/卖方双视角：所有对外材料是卖方产物，分析师永远切到买方验，差额即本质 | 硬约束，凡读自利信源 |

## 怎么在 SKILL.md 里引用

各 analyst-* skill 的 SKILL.md 不要复制粘贴这些内容，而是引用：

```markdown
## 方法论（必读）

本 skill 严格遵守分析师团队共享方法论：

- 四大铁律：见 `methodology/00-ironclad-rules.md`
- 五种核心能力：见 `methodology/01-five-capabilities.md`
- Plain-Speak 表达：见 `methodology/02-plain-speak.md`
- Handoff Hints：见 `methodology/03-handoff-hints.md`
```

（`methodology/` 在每个 skill 目录里是个 symlink → `~/analyst-skills/shared/methodology/`）

## 修改约定

改这些文件前，先想：
- 这是真正通用的（所有分析师都要遵守）吗？
- 还是只对某个 skill 适用？

如果只对某 skill 适用 → 放在 skill 自己的目录里，不要污染 shared/。
如果是通用的 → 改这里，记一笔到 项目 decisions（内部，未公开）。
