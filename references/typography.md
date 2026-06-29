# 排版规范（微信公众号适配）

## 输出格式
- **必须输出DOCX格式**，使用docx-js（JavaScript）生成
- 输出文件保存到 `outputs/` 目录

## 微信公众号排版标准

**字号**：正文14px(10.5pt)、标题16-20px(12-15pt)
**颜色**：正文 `#3f3f3f`、标题 `#1a1a1a`、强调红 `#B5493A`、辅助灰 `#999999`，全篇≤3种颜色
**间距**：行距1.5-1.75倍、段后12pt、章节间24pt
**对齐**：不首行缩进、两端对齐、段间空一行
**图片**：宽900px、每300-500字一张、两侧留10px边距

## docx-js参数

```javascript
const TITLE_SIZE = 30;      // 15pt (半磅单位)
const SUBTITLE_SIZE = 24;   // 12pt
const BODY_SIZE = 21;       // 10.5pt
const CAPTION_SIZE = 18;    // 9pt
const LINE_SPACING = 384;   // 1.6倍 (240*1.6)
const PARA_AFTER = 240;     // 12pt
const SECTION_AFTER = 480;  // 24pt
const PAGE_MARGIN = 1418;   // 2.5cm (567*2.5)
```

## 特殊模块（用表格实现）
- `dataCard()`：数据卡片，灰色底+红色高亮
- `highlightBox()`：高亮框，核心观点
- `contrastBox()`：左右对比框，荒诞对比
- `quoteBox()`：引用框，黄色左边框+斜体
- `makeTable()`：数据表格，表头灰色底
- `ctaBox()`：引流框，红色边框+粉色底
- `divider()`：虚线分隔符
