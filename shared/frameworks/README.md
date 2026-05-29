# shared/frameworks — 跨 skill 通用分析框架

这些框架对 **analyst-tech / analyst-business / analyst-media 都适用**。
各 skill 的 SKILL.md 可以按需引用。

skill 专属的框架（如 analyst-tech 的 TRL、IP-Landscape）放在 skill 自己的 `frameworks/` 目录里，不在这里。

---

## 框架地图

| 框架 | 一句话用途 | 何时调用 | 详见 |
|---|---|---|---|
| **First Principles** | 拆到不可再拆的物理 / 经济 / 信息约束做 sanity check | 任何"看起来太好 / 太丑" 的判断；量纲检查 | [first-principles.md](first-principles.md) |
| **Lateral-Vertical** | 纵向 why×5 + so what×5；横向跨域类比 | 每次分析必用——五种核心能力的 #3 #4 | [lateral-vertical.md](lateral-vertical.md) |
| **Historical Timeline** | 找 3-7 个真正改变集体认知的转折点 | 任何涉及"演化 / 趋势 / 趋势性判断" 的分析必用——五种核心能力的 #5 | [historical-timeline.md](historical-timeline.md) |
| **Hype Cycle** | Gartner 五阶段炒作曲线，定位"现在在炒作哪一步" | 评估"是不是炒作 / 是不是真起来了" | [hype-cycle.md](hype-cycle.md) |
| **S-Curve** | 技术 / 产品 / 市场的成长饱和曲线 | 评估"现在在 S 曲线哪段 / 下一段是什么" | [s-curve.md](s-curve.md) |
| **Crossing the Chasm** | 早期市场 vs 主流市场之间的鸿沟 | 评估商业化时机、市场扩散阶段 | [crossing-the-chasm.md](crossing-the-chasm.md) |

---

## 选用规则

- **First Principles + Lateral-Vertical + Historical Timeline 是每次任务的最低标准**（五种核心能力的后三种就是它们）
- Hype Cycle / S-Curve / Crossing-the-Chasm 按问题类型挑选——见各 skill 自己的 workflow.md 里的"问题类型 → 框架"映射
- 框架是工具不是教条。**如果某框架不适合当前问题，说明为什么不用比硬套更专业。**
