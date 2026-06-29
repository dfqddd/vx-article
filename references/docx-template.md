# DOCX生成脚本模板

## 基础模板（docx-js / JavaScript）

```javascript
const fs = require('fs');
const { Document, Packer, Paragraph, TextRun, Table, TableRow, TableCell,
        AlignmentType, BorderStyle, WidthType, ShadingType } = require('docx');

const TITLE_SIZE = 30;      // 15pt
const SUBTITLE_SIZE = 24;   // 12pt
const BODY_SIZE = 21;       // 10.5pt
const BODY_COLOR = "3f3f3f";
const TITLE_COLOR = "1a1a1a";
const ACCENT_COLOR = "B5493A";
const MUTED_COLOR = "999999";
const LINE_SPACING = 384;
const PARA_AFTER = 240;
const SECTION_AFTER = 480;
const PAGE_MARGIN = 1418;   // 2.5cm

function p(text, options = {}) {
  return new Paragraph({
    children: [new TextRun({
      text, size: BODY_SIZE, color: BODY_COLOR, font: "PingFang SC", ...options.run
    })],
    spacing: { line: LINE_SPACING, after: PARA_AFTER, ...options.spacing },
    alignment: options.alignment || AlignmentType.LEFT,
  });
}

function emphasis(text) {
  return new TextRun({ text, bold: true, color: ACCENT_COLOR, size: BODY_SIZE, font: "PingFang SC" });
}

function divider() {
  return new Paragraph({
    children: [new TextRun({ text: "· · ·", size: BODY_SIZE, color: MUTED_COLOR, font: "PingFang SC" })],
    alignment: AlignmentType.CENTER,
    spacing: { before: SECTION_AFTER, after: SECTION_AFTER }
  });
}

const doc = new Document({
  styles: { default: { document: { run: { size: BODY_SIZE, color: BODY_COLOR, font: "PingFang SC" } } } },
  sections: [{
    properties: { page: { margin: { top: PAGE_MARGIN, right: PAGE_MARGIN, bottom: PAGE_MARGIN, left: PAGE_MARGIN } } },
    children: [
      new Paragraph({
        children: [new TextRun({ text: "文章标题", bold: true, size: TITLE_SIZE, color: TITLE_COLOR, font: "PingFang SC" })],
        alignment: AlignmentType.CENTER, spacing: { after: SECTION_AFTER }
      }),
      p("正文段落..."),
      divider(),
    ]
  }]
});

Packer.toBuffer(doc).then(buffer => {
  fs.writeFileSync("outputs/文章标题.docx", buffer);
  console.log("生成成功");
});
```

## 特殊模块（用Table实现）

- `dataCard()`：1行1列灰色背景，红色高亮关键数据
- `highlightBox()`：浅色背景+左边框，核心观点
- `contrastBox()`：2列左右对比，制造荒诞对比
- `quoteBox()`：左边框3pt黄色+斜体
- `makeTable()`：表头行灰色背景
- `ctaBox()`：红色顶部和底部边框+粉色底

## 每日热点速评极简版

```javascript
// 标题
children.push(new Paragraph({
  children: [new TextRun({ text: "标题文字", bold: true, size: 40 })],
  alignment: AlignmentType.CENTER, spacing: { after: 400 }
}));
// 编号段落
children.push(p("1. 热点内容...", { spacing: { before: 240, after: 120 } }));
// 结尾引导
children.push(p("你觉得xxx？评论区说说。", { spacing: { before: 240 } }));
```
