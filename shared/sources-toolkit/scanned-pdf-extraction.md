# 扫描版 / 乱码 PDF 的文本抽取 SOP

**适用所有 analyst-***。首次浮现：商业模式分析 dogfood（港交所招股书）。

## 触发条件（命中任一即走本 SOP，别再硬试 WebFetch）

- WebFetch 返回"PDF 结构/图像流、无实质文本" → 图像型扫描 PDF
- 抽出的文本是乱码 `ҁ዆Ͼˏ`（mojibake）→ 嵌了自定义字体、CMap 不映射 Unicode（**港交所招股书几乎都这样**）
- `pdftotext` 跑了但输出为空

**英文/数字常能漏出来**（公司英文名、百分比），可用来先确认身份；中文正文必须走下面的渲染路线。

## 首选方法：PyMuPDF 渲染成图 → 视觉读（不依赖 OCR 工具链）

比 tesseract 准得多（中文财报表格 tesseract 质量差），且能定点。

```bash
python3 -m pip install --quiet --user pymupdf   # 只需这一个，无系统依赖
python3 - "$PDF" "$OUTDIR" <<'PY'
import sys, fitz
pdf, out = sys.argv[1], sys.argv[2]
doc = fitz.open(pdf); print("pages:", doc.page_count)
for i in PAGE_LIST:                       # 定点渲染目标页，别全文渲
    doc[i].get_pixmap(dpi=150).save(f"{out}/p{i:03d}.png")   # 密集表格用 dpi>=220
PY
```

然后用 **Read 工具读 PNG**（Read 能视觉解析图片），逐页抽取。

## 关键技巧

1. **先渲染目录页定位章节**，别盲读 300+ 页。读到目录后建立"章节→招股书内页码"映射。
2. **PDF 索引 ≠ 招股书内页码**：前置页（封面/释义/目录用罗马数字）造成偏移。某招股书实例：`PDF索引 ≈ 内页码 + 8`。先渲染一页核对偏移量再批量。
3. **DPI 分级**：概要/正文 150 够；财务三表、密集表格用 ≥220 重渲（文件名加 `hi_` 区分）。
4. **港交所申请版本(A1)的 `[編纂]` = 打码**：发行规模、募资金额明细、基石投资者在 A1 阶段通常打码；**用途类别/百分比的文字描述一般可见**。打码本身是一条 finding（PHIP/正式版才解码）。
5. 高价值章节优先级（招股书通用）：**概要**（浓缩 pitch+财务高亮，单段 ROI 最高）> 未来计划及募资用途 > 财务资料/会计师报告（capex/折旧/供应商集中度）> 业务（模式/客户/供应链）> 风险因素（"认罪书"）。

## 次选：tesseract OCR（仅当需要大批量文本检索时）

需系统安装，且中文表格质量差：
```bash
brew install poppler tesseract tesseract-lang   # 装 chi_tra/chi_sim 语言包
python3 -c "from pdf2image import convert_from_path; import pytesseract; ..."
```
**不推荐**作为首选——渲染+视觉读更准更快。

## 何时 M-xxx

登录态/付费墙/文件下不下来 → M-xxx 请用户提供本地文件路径或截图。
