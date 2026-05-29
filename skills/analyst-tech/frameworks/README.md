# 分析框架索引与选用决策树

本目录是技术分析师的"工具箱"。**先选框架，再动手**——这是铁律。

框架分两类：
- **思维方法类**（first-principles, lateral-vertical, historical-timeline）：每次任务**都要用**，不是可选
- **领域分析类**（hype-cycle, 7 powers 等）：按问题类型选用

## 框架选用决策树

```
任何任务：
默认必用 → first-principles.md + lateral-vertical.md + historical-timeline.md
                                              │
                                              ↓
问题类型 → 叠加对应领域框架：

├── 「这技术成熟了吗？」
│   ├── 主用：Hype Cycle (hype-cycle.md)
│   ├── 辅助：S-Curve (s-curve.md)
│   └── 辅助：TRL 技术成熟度等级 (trl.md)
│
├── 「这技术有壁垒/护城河吗？」
│   ├── 主用：7 Powers (moat-analysis.md)
│   └── 辅助：IP Landscape (ip-landscape.md)
│
├── 「这家公司技术怎么样？做技术 DD」
│   ├── 主用：Technical DD Checklist (technical-due-diligence.md)
│   ├── 辅助：Moat Analysis (moat-analysis.md)
│   └── 辅助：IP Landscape (ip-landscape.md)
│
├── 「技术路线 A vs B 哪个会赢？」
│   ├── 主用：Wardley Mapping (wardley-mapping.md)
│   ├── 辅助：S-Curve (s-curve.md)
│   └── 辅助：Crossing the Chasm (crossing-the-chasm.md)
│
├── 「现在是不是好时机？」
│   ├── 主用：Hype Cycle + Crossing the Chasm
│   ├── 辅助：S-Curve（看是否在曲线拐点）
│   └── 辅助：Why Now? 三要素分析
│
├── 「专利和 IP 怎么样？」
│   └── 主用：IP Landscape + FTO (ip-landscape.md)
│
└── 「这个数字 / 主张看起来太美 / 太丑了」
    └── **必用：First-Principles 做 sanity check**
```

## 思维方法（每次都用）

| 框架 | 一句话用途 | 文件 |
|---|---|---|
| **First-Principles** | 拆到不可再拆的物理/经济/信息约束，做 sanity check | `first-principles.md` |
| **Lateral-Vertical** | 纵向 why × 5 / so what × 5 + 横向类比对照 | `lateral-vertical.md` |
| **Historical-Timeline** | 找 3-7 个关键认知转折点（不是流水账日期） | `historical-timeline.md` |

## 领域框架（按问题类型选）

| 框架 | 一句话用途 | 主要适用场景 | 文件 |
|---|---|---|---|
| **Technical DD Checklist** | 系统化技术尽调 7 维度 | 投前技术评估 | `technical-due-diligence.md` |
| **Hype Cycle** | 判断技术处在炒作周期哪个阶段 | 技术趋势研判、时机判断 | `hype-cycle.md` |
| **7 Powers** | 解析技术企业的 7 种护城河来源 | 护城河分析、竞争评估 | `moat-analysis.md` |
| **S-Curve** | 看技术演进是否触顶、新曲线在哪 | 技术替代判断 | `s-curve.md` |
| **Wardley Mapping** | 价值链 + 演化阶段可视化 | 战略与路线判断 | `wardley-mapping.md` |
| **Crossing the Chasm** | 创新采用周期，识别"鸿沟"位置 | 商业化时机判断 | `crossing-the-chasm.md` |
| **TRL** | NASA/DARPA 系技术成熟度 1-9 级 | 硬科技/早期技术评估 | `trl.md` |
| **IP Landscape** | 专利图谱与 FTO 自由实施 | 涉及核心 IP 的赛道 | `ip-landscape.md` |

## 何时组合使用

单一框架往往只能回答一个维度。严肃的分析通常需要"思维方法 + 2-3 个领域框架"交叉：

- **「这家公司的技术底色如何」** = First-Principles + Lateral-Vertical + Technical DD + 7 Powers + IP Landscape
- **「这项技术现在的真实位置」** = First-Principles + Lateral-Vertical + Hype Cycle + Crossing the Chasm + S-Curve
- **「路线 A 还是 B 更可能赢」** = First-Principles + Lateral-Vertical + Wardley Mapping + S-Curve + 7 Powers
- **「这项技术能不能跨越鸿沟」** = First-Principles + Lateral-Vertical + Crossing the Chasm + TRL + Hype Cycle

## 不要做的事

- **不要跳过思维方法**。三个思维框架（First-Principles + Lateral-Vertical + Historical-Timeline）是地基，没有它们的分析等于"按框架填空"。
- **不要每次都用 SWOT**。SWOT 适合战略对话，不适合技术尽调——太粗、太主观。
- **不要硬套不合适的框架**。如果发现框架不贴合，明确写出"为什么不用"反而显专业。
- **不要罗列框架定义**。框架不是给读者上课用的，是给你自己组织思考用的。读者只看你的判断。
- **不要用 jargon 墙糊弄**。Plain-Speak 双层表达是输出层铁律——首次出现的核心术语必带"用大白话说" 版本。
