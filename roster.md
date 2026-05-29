# Roster — 分析师矩阵

每个 analyst-* skill 的状态、定位、差异化记录。

## 状态说明

- **draft** — 草稿期，结构未稳定
- **iterating** — 在迭代，方法论会变
- **stable** — 已稳定，主要做小修补
- **planned** — 计划中，尚未开始
- **deprecated** — 已废弃

## 当前矩阵

| Skill | 状态 | 角色定位 | 触发场景 | 路径 |
|---|---|---|---|---|
| **analyst-tech** | iterating | 中立技术真相判断者 | 技术 / 技术公司 / 技术路线 / 技术趋势的评估与判断 | `~/.claude/skills/analyst-tech/` |
| **analyst-people** | iterating | 还原一个人的审美 | 作家 / 画家 / 投资人 / 创业者 / 科技人物 等创造性 / 决策性人物 | `~/.claude/skills/analyst-people/` |
| **analyst-business** | iterating | 卖买双视角拆商业模式 | 一家公司怎么赚钱 / 护城河真假 / 值不值这个价；尤其 IPO·招股书·财报 | `~/.claude/skills/analyst-business/` |
| **analyst-media** | planned | 媒体视角评估 | 叙事、时机、独家性、选题 | — |

## 差异化

| 维度 | analyst-tech | analyst-people | analyst-business | analyst-media |
|---|---|---|---|---|
| 核心问题 | "这技术是不是真的 / 有多成熟？" | "这个人怎么想 / 怎么走来的 / 走向哪？" | "这门生意怎么赚钱 / 值不值这个价？" | "这是不是好故事 / 怎么讲？" |
| 输出重心 | 技术判断 + 信心等级 | 审美 + 思维模式 + 心路历程 + 来时路 + 未来路径 | 卖方-买方并排 thread + 估值裁决 | 叙事角度 + 时机窗口 |
| 信源偏重 | 论文、专利、benchmark、招股书 | 本人言论 + 事件库 + 关系网 | 招股书 / 财报三表 / 风险因素 / 可比公司 / 客户行为 | 媒体先例、读者反响、独家信源 |
| Handoff 模式 | 产出 hints 给另外两人 | 独立工作 / 可与 business/media 互补（人 ↔ 公司 ↔ 故事） | 消费 tech 的 hints | 消费 tech 的 hints |

## 共享 vs 专属

所有 analyst-* 都共享 `shared/`：方法论铁律、通用框架（第一性、纵横向、历史时间轴等）、信源分级、模板骨架、工作流骨架。

各自专属：
- **analyst-tech**：TRL、Tech-DD、IP-Landscape、Moat-Analysis、Wardley、学术信源
- **analyst-people**：5 种审美痕迹（选择/评价/模仿/不可妥协/演变）、4 阶段工作流（信源勘探 → 言论事件库 → 审美痕迹 → 四画像）、M-xxx 接力协议
- **analyst-business**：卖方-买方双视角（sell-buy-dialectic）、真实力度量栈（透过包装看本质·裸算力案例）、交易层取证锚（IPO/招股书 readout + 从价钱倒推）、卖买并排 thread 模板
- **analyst-media**：（待定）叙事框架、媒体先例库、读者画像

> 命名沿革：`analyst-business` 由原计划中的 `analyst-business` 收窄重定位而来——入口从"投资视角泛评估"改为"卖买双视角拆商业模式"。（收窄重定位见项目 decisions）。
