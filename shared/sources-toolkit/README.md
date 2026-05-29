# Sources Toolkit

> 信息源 / 抓取入口 / 数据库的共享工具集。所有 analyst-* skill 共享。
> 首次浮现：人物分析 dogfood

## 顶层约束

> **零付费 API**。一切付费瓶颈走用户 M-xxx 手动接力。

来源：用户明示（"我们全部都是走免费路径，不额外花钱。然后实在不行我手工去复制粘贴。"）。

## 目录结构（雏形，按需补）

```
sources-toolkit/
├── README.md                  ← 本文档（索引 + 决策树 + 约束）
├── platforms/                 ← 平台抓取入口（每平台一篇）
│   └── （按需补：wechat / weibo / zhihu / jike / xiaoyuzhou / twitter-x / linkedin / substack / youtube / bilibili / medium）
├── databases/                 ← 人物 / 公司 / 投资数据库
│   └── （按需补：itjuzi / qichacha-tianyancha / crunchbase / wikipedia-wikidata）
├── academic/                  ← 学术 / 专利
│   └── （按需补：semantic-scholar / arxiv-crossref / google-patents）
├── media-rss/                 ← 中文科技媒体 RSS
│   └── （按需补：china-tech-media）
└── aggregators/               ← 聚合 / 兜底工具
    └── （按需补：rsshub / archive-wayback / search-engines）
```

## 平台笔记模板

每个文件遵循以下结构：

```markdown
# [平台 / 服务名]
- **类型**：公开 / 付费 / 开源工具
- **入口**：URL / API endpoint / repo
- **调用方式**：[具体怎么用，含命令样例]
- **限速 / 配额 / 反爬**：[实际限制]
- **已知坑**：[踩过的雷]
- **用例**：[查询某人 / 某事的实际命令]
- **状态**：✅ 验证可用 / ⚠️ 待核实 / ❌ 已失效（日期）
```

## "以一抵百"工具（优先文档化）

| 工具 | 为什么强调 |
|---|---|
| **RSSHub** | 开源，已为微信 / 微博 / 即刻 / 小宇宙 / 知乎 / B 站 / Twitter 等几百个源生成 RSS。命中"开源入口"约束 |
| **yt-dlp** | 任何视频 / 音频 → 字幕提取（YouTube / B 站自带字幕直接拿，无需 whisper 付费） |
| **Wayback Machine** | 救回被删 / 改写内容。⚠️ **注意：Claude Code WebFetch 当前不可达 web.archive.org**（2026-05-25 实测沙箱阻止），需用其他途径或 M-xxx 接力 |

## 已识别的"必走 M-xxx 接力"场景

由实战 dogfood 识别：

| 场景 | 原因 | 接力成本估计 |
|---|---|---|
| 微信公众号全量历史列表 | 无官方路径、第三方都不稳 | 8-12 分钟 |
| 知乎专栏（zhuanlan.zhihu.com）| 反爬 403（实测） | 5 分钟 |
| LinkedIn 完整履历 | 反爬严重，无免费可靠替代 | 8 分钟 |
| 朋友圈 / 知识星球 | 登录态 + 付费墙 | 5-10 分钟 |
| 长视频 / 播客无字幕 | whisper 转写本地慢、API 付费 | 用户挑关键段 |
| 圈内传言 / 私下口碑 | 不在公开互联网 | 用户找熟人侧证 |

## 已识别的"绕开"路径（不是必走接力）

由实战 dogfood 发现：

- **微信公众号文章**虽然全量列表抓不到，但**绝大多数关键文章在第三方平台被转载**（腾讯新闻 / 网易 / 知乎 / 53AI / 极客公园 / aitntnews / 经管之家）—— **先搜转载源，再 fetch**
- **官方 X 账号**虽然 x.com 直 fetch 经常 503，但可用 Nitter 镜像或 M-xxx 接力
- **机构（投研机构 / 创业公司）**往往有**自有官网 + Newsletter**，这是最权威的一手源，**优先于公众号**
- **投研机构官网研报正文订阅墙**——但**标题 / 摘要 / 阅读指引**通常可抓，标签层信息也是审美信号

## 决策树：要抓 X，去哪？

```
                 ┌─→ 自有官网 / Newsletter? ──→ 优先 fetch（最一手）
                 │
某人 / 某事 ────┤
                 ├─→ 转载平台有吗? ──→ fetch 转载（绕开公众号难抓）
                 │
                 ├─→ 播客 / 视频? ──→ 找带字幕的；没字幕则 M-xxx 用户挑段
                 │
                 ├─→ 短文（X / 即刻 / 微博）? ──→ 试 Nitter 镜像 / RSSHub；不行 M-xxx
                 │
                 ├─→ 数据库（工商 / 投资）? ──→ 启信宝 / 36氪 PitchHub（免费层）
                 │
                 └─→ 都拿不到? ──→ M-xxx 接力 / 标缺口 / 不推理
```

## 边跑边沉淀（不预先空写）

最先要补的（已识别 — Phase 2 of toolkit dev）：

- [ ] `platforms/wechat.md`（实战遇过多种绕开方式）
- [ ] `platforms/zhihu.md`（实战遇过 403）
- [ ] `platforms/xiaoyuzhou.md`（实战拿过节目列表）
- [ ] `aggregators/wayback.md`（实战发现 Claude Code 沙箱阻止）
- [ ] `platforms/twitter-x.md`（实战遇过 503）
- [ ] `platforms/substack.md`（标准 RSS — 最干净的国际源）
- [ ] `aggregators/rsshub.md`（万能 RSS — "以一抵百"详细文档）

## 状态

v0.1（2026-05-25）— 雏形 + 顶层约束 + 已识别路径列出
v0.2 计划 — 上面 [ ] 列表补 platform notes
v0.3 计划 — 跨 analyst-* skill 实战后补 databases / academic 类
