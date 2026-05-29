# 学术信源（Tier 1）

判断技术真实成熟度、追溯创新源头、识别 SOTA 的核心信源。

## 论文数据库

| 数据库 | 覆盖 | URL | 适用 |
|---|---|---|---|
| **arXiv** | 物理、CS、数学、生物等预印本 | arxiv.org | 最新研究（含未评审） |
| **Google Scholar** | 全学科 + 引用追踪 | scholar.google.com | 引用网络、综述 |
| **Semantic Scholar** | AI/CS 强化、含影响力评分 | semanticscholar.org | AI 领域首选 |
| **Papers with Code** | 论文 + 代码 + benchmark | paperswithcode.com | 验证可复现性 |
| **DBLP** | CS 论文索引 | dblp.org | 找作者全部产出 |
| **PubMed** | 生物医学 | pubmed.ncbi.nlm.nih.gov | 生医必查 |
| **IEEE Xplore** | 电气电子、通信 | ieeexplore.ieee.org | 硬件、芯片、通信 |
| **ACM Digital Library** | CS 期刊会议 | dl.acm.org | 计算机理论与系统 |
| **SSRN** | 经济、金融、法律 | ssrn.com | 跨学科研究 |

## 顶级会议（按领域）

### AI/ML 综合
- **NeurIPS**（神经信息处理）— 年度盛会
- **ICML**（机器学习）— 偏理论
- **ICLR**（表示学习）— Open Review，可看审稿
- **AAAI**（人工智能综合）
- **IJCAI**（国际人工智能）

### 自然语言处理
- **ACL / EMNLP / NAACL**
- **TACL**（期刊）

### 计算机视觉
- **CVPR / ICCV / ECCV**

### 系统与基础设施
- **OSDI / SOSP**（操作系统）
- **NSDI / SIGCOMM**（网络）
- **VLDB / SIGMOD**（数据库）
- **MLSys**（ML 系统）

### 机器人
- **ICRA / IROS**（综合）
- **CoRL**（机器人学习）
- **RSS**（Robotics: Science and Systems）

### 安全
- **USENIX Security / S&P / CCS / NDSS**

### 芯片与硬件
- **ISSCC**（国际固态电路）— Intel/AMD/台积电公开技术的舞台
- **ISCA / MICRO / HPCA / ASPLOS**（计算机体系结构）

### 生物医药
- **Nature / Science / Cell** 主刊及子刊
- **NEJM**（医学）
- **AAAS / AACR**（年会）

## 评估论文质量的快速法

1. **作者机构与背景**：顶尖实验室 ≠ 论文一定好，但失败率显著低
2. **引用数与影响力分数**：Semantic Scholar 的"高影响力引用"比单纯引用数更准
3. **代码 + 数据是否公开**：Papers with Code 验证可复现性
4. **被后续 SOTA 论文引用的方式**：被引用为"基线"、"改进起点"、"批判对象"含义不同
5. **审稿意见**（ICLR / OpenReview 可见）

## 跟踪研究前沿的工作流

### 日常追踪

1. **每周扫 arXiv** 的相关 category（cs.AI, cs.CL, cs.CV, cs.LG, cs.RO 等）
2. **订阅 newsletter**：
   - The Batch (DeepLearning.AI) — 综合
   - Import AI (Jack Clark) — 政策 + 技术
   - Last Week in AI — 综合
   - Ahead of AI (Sebastian Raschka) — 深度技术
3. **关注 Twitter/X 学术圈**：核心实验室 PI、明星博士生

### 主题深挖

1. 找 1-2 篇主题"种子论文"（最近 12 个月内发表的高引论文）
2. 用 Google Scholar 反向追踪："谁引用了它"
3. 用 Semantic Scholar 的"Influential Citations" 过滤
4. 找该作者的"近 3 年其他工作"，看研究方向轨迹

## 顶尖实验室与团队（快速检索锚点）

### 工业实验室
- **Anthropic, OpenAI, DeepMind, Meta FAIR, Microsoft Research**
- **Google Research, Apple ML Research, NVIDIA Research**
- **Tencent AI Lab, ByteDance AI Lab, Alibaba DAMO, 华为诺亚方舟实验室**
- **百度研究院、智源研究院 (BAAI)、上海人工智能实验室**

### 学术实验室（AI 方向举例）
- Stanford SAIL / HAI
- Berkeley AI Research (BAIR)
- MIT CSAIL
- CMU AI / Robotics Institute
- 清华 THUNLP / 智源
- 北大、上交、中科院相关团队
- ETH AI Center, MILA (Montreal)

## 中文学术信源

- **CNKI / 知网** — 中文论文最全
- **万方 / 维普** — 替代选择
- **中国知网开放科学数据库**
- **国家自然科学基金（NSFC）项目查询** — 看政府资助风向

## 用学术信源时常见的错误

1. **看不出"论文级别"差距**。一篇 arXiv preprint ≠ 一篇 NeurIPS Oral，差异巨大。
2. **被 demo 蒙蔽**。论文 figure / video 经常 cherry-picked。要找独立复现。
3. **不看作者轨迹**。同一作者的工作连续性是判断技术稳定性的关键。
4. **不查"勘误 / 撤稿"**。被撤稿的论文仍可能在引用网络中流传。
5. **忽略综述（survey）论文**。一篇好综述能省 20 篇论文的阅读时间。
