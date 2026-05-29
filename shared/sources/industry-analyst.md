# 行业分析机构与研报（Tier 2）

成熟方法论 + 系统化数据。适合做市场规模、采用率、技术成熟度等量化判断的起点。

## 国际综合研究

| 机构 | 强项 | 主要免费内容 | 付费层级 |
|---|---|---|---|
| **Gartner** | 技术成熟度（Hype Cycle、Magic Quadrant）| 摘要、新闻稿 | 单份报告 $$ ~ $$$$$ |
| **Forrester** | 企业软件、客户体验、AI 应用 | 摘要 | 同上 |
| **IDC** | 硬件市场、企业 IT、电信 | 部分免费 | 单份报告 $$ ~ $$$$ |
| **CB Insights** | 创投数据、AI 与新兴科技图谱 | 周报 + 部分 brief | 订阅 $$$ |
| **PitchBook** | 创投、PE、M&A 数据 | 摘要 | 高价订阅 |
| **Crunchbase** | 公司基础数据、融资 | 大部分免费 | 订阅 $$ |
| **S&P / Refinitiv / Bloomberg** | 金融市场、上市公司 | 终端付费 | 终端 |

## VC 与战略类研究

| 机构 / 人 | 类型 | URL |
|---|---|---|
| **a16z** | 长文 + 投资主题 | a16z.com |
| **Sequoia / Sequoia China** | 创业者公开信、行业图谱 | sequoiacap.com |
| **Bessemer (BVP) State of the Cloud** | SaaS 年度状态 | bvp.com |
| **Coatue Tech Annual** | 二级科技市场 | coatue.com |
| **Andreessen Horowitz Index** | 跨主题研究 | 同上 |
| **Lightspeed / Insight Partners** | 主题报告 | 各自官网 |
| **NFX Briefs** | 网络效应 | nfx.com |
| **The Generalist** | 公司深度 | readthegeneralist.com |
| **Not Boring (Packy McCormick)** | 公司深度 | notboring.co |
| **Stratechery (Ben Thompson)** | 商业战略 | stratechery.com |
| **The Information** | 科技业内深度 | theinformation.com（付费） |
| **Benedict Evans** | 趋势综合 | ben-evans.com |

## 投行研报

- **Goldman Sachs, Morgan Stanley, J.P. Morgan**（科技 / TMT 组）
- **中金 (CICC)、中信、申万、海通**（A 股 + 港股科技覆盖）
- **大摩中国 / 高盛中国**（中概股覆盖）

**获取路径**：彭博 / Refinitiv 终端、券商客户内部、行业邮件列表，或财经网站二手摘要。

## 中国本土研究机构

| 机构 | 类型 | 强项 |
|---|---|---|
| **中国信通院 (CAICT)** | 政府智库 | 通信、AI、云计算白皮书 |
| **赛迪研究院 (CCID)** | 政府智库 | 芯片、电子信息 |
| **艾瑞咨询 (iResearch)** | 商业研究 | 互联网、消费 |
| **易观分析** | 商业研究 | 移动互联网、金融科技 |
| **QuestMobile** | 商业研究 | 移动 App 数据 |
| **比达咨询 (BigData-Research)** | 商业研究 | 移动应用 |
| **沙利文 (Frost & Sullivan)** | 国际化分公司 | 招股书引用最多 |
| **IT 桔子** | 创投数据 | 中国 startup 融资 |
| **零壹智库 / 36Kr 研究院** | 商业研究 | 金融科技、产业互联网 |
| **甲子光年 / 智库** | 商业研究 | AI、新基建 |

## 如何高效"扒研报"

### 检索路径

1. **公司招股书披露**：上市公司在 IPO 招股书 / 重大事项公告里会大量引用 Frost & Sullivan、IDC、艾瑞等数据 → 直接搜公司 + 招股书可获得整段引用
2. **会议演讲 / 媒体引用**：行业大会、媒体报道里常会引用最新研报数据
3. **机构的免费版报告**：多数大机构每季度发 1-2 份 free brief
4. **学术论文中的市场综述章节**
5. **付费替代**：研报代下载平台（合规性自行判断）

### 验证研报数据

研报数据看似权威但常有问题：
- **统计口径**：同一"AI 市场"，不同机构差 5 倍很常见。一定要看口径定义
- **时点**：研报发布时间 vs 数据截止时间常常错位
- **预测 vs 实际**：3 年前的预测今天对照实际偏差多少？看历史预测准度
- **付费方利益**：很多研报是甲方付费请第三方做的（招股书引用 Frost & Sullivan 的报告，多是公司付钱定制的）

### 多源对照规则

涉及市场规模的数据，**至少 3 个独立机构对照**。如果差异巨大（>30%），不要直接选一个，而要：
- 用区间表达：「XX 机构估算 5000 亿元，YY 机构估算 3000 亿元，差异主要来自……」
- 给出"自我估算逻辑"（自下而上从客户数 × ARPU 推算）

## Hype Cycle 与 Magic Quadrant 的正确用法

### Hype Cycle
- 表征行业**集体认知**的相对位置，不直接是技术成熟度
- 同一技术在不同 Gartner 报告间位置常变化，要看演化轨迹

### Magic Quadrant
- 横轴"前瞻性 (vision)" 纵轴"执行力 (ability to execute)"
- 不要只看四象限位置，要看上一年到当年的"移动方向"
- 注意 Gartner 的客户付费关系（Magic Quadrant 不是纯独立评估）

## 用研报时常见的错误

1. **拿研报当事实，不当假设**。研报是"专业的猜测"，不是地面真相。
2. **混淆 TAM 与 SAM**。研报中的"市场规模"经常是 TAM，远大于真实可获得的 SAM。
3. **忽视统计口径**。不同口径下的同一数据差异巨大。
4. **过度信任头部机构**。Gartner / Forrester 也经常错（如对元宇宙的 2022 年预测）。
5. **不交叉中文研报**。中国市场的真实数据，中文研报往往更接近事实。
