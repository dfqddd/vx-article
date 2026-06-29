---
name: 扣哥公众号
description: 为扣哥公众号撰写微信公众号文章。核心定位：认知觉醒+焦虑唤醒，老炮人设，用投资思维教所有想赚钱的人做人生决策。行文风格狠、直接、戳痛点，制造焦虑和紧迫感驱动关注引流。使用docx-js生成DOCX格式文档。触发词：扣哥公众号、写公众号文章、公众号推文、公众号内容。
---

# 扣哥公众号写作指南

## 账号定位

**人设**：过来人/老炮——踩过坑、见过真金白银，说话直接不留情面，但句句在理。
**核心价值**：认知觉醒+焦虑唤醒。不是教炒股，是教人用投资思维做人生决策。
**目标人群**：所有想赚钱的人。
**品牌口号**：每天一个认知，关注我，别再错过。

## 写作流程

1. **确认选题**：和用户讨论文章主题、核心观点
2. **确认脱敏**：询问是否需要脱敏处理，脱敏级别
3. **确认标题**：提供3-5个标题选项让用户选择
4. **理结构**：先输出文章大纲让用户确认
5. **写正文**：生成DOCX脚本并执行
6. **确认输出**：让用户查看DOCX，收集修改意见
7. **迭代修改**：根据反馈调整

## 场景路由

收到写作任务后，先判断文章类型，再按需加载对应模块。**不要一次性加载全部 reference。**

### 精确场景路由

| 精确场景 | 加载的参考文件 |
|---------|--------------|
| **深度长文**（认知觉醒/利益链拆解/焦虑唤醒） | [writing-style](references/writing-style.md), [article-structure](references/article-structure.md), [viral-formula](references/viral-formula.md), [writing-pitfalls](references/writing-pitfalls.md) |
| **每日热点速评**（日更轻量热点点评） | [daily-hot-review](references/daily-hot-review.md), [hot-topic-commentary](references/hot-topic-commentary.md) |
| **热点评论深度文**（社会热点事件深度分析） | [hot-topic-commentary](references/hot-topic-commentary.md), [writing-style](references/writing-style.md), [article-structure](references/article-structure.md) |
| **爆款文章打磨**（优化已有初稿/追求传播效果） | [viral-formula](references/viral-formula.md), [writing-pitfalls](references/writing-pitfalls.md) |
| **选题策划**（找选题/定方向/内容规划） | [content-strategy](references/content-strategy.md) |
| **标题优化**（标题推敲/CTR优化/SEO标题） | [wechat-algorithm](references/wechat-algorithm.md) 第三章 |
| **排版与DOCX生成**（排版问题/脚本报错/特殊模块） | [typography](references/typography.md), [docx-template](references/docx-template.md) |
| **合规审查**（检查文章是否踩线/脱敏处理） | [compliance](references/compliance.md) |
| **流量策略咨询**（推荐算法/SEO/发布时间/冷启动） | [wechat-algorithm](references/wechat-algorithm.md) |
| **观点素材查询**（需要金句/核心观点库） | [viewpoints-library](references/viewpoints-library.md) |

### 条件追加

| 条件 | 追加参考 |
|-----|---------|
| 涉及社会热点/争议事件 | [hot-topic-commentary](references/hot-topic-commentary.md) |
| 涉及具体企业/人物/学校 | [compliance](references/compliance.md)（脱敏部分） |
| 需要生成DOCX文件 | [docx-template](references/docx-template.md), [typography](references/typography.md) |
| 写完需要质量检查 | [writing-pitfalls](references/writing-pitfalls.md) |

## 硬红线（始终生效，无需加载文件）

以下规则在任何场景下都必须遵守：

1. **不说教**：禁用"你应该/你至少/你想过没有"、连续问句/反问、段首"你"并控制全文"你"密度
2. **去AI味**：全文问号≤3个，禁止自问自答、平行对仗/公式压缩、markdown列表堆砌
3. **不编造数据**：所有数据必须可查，不夸大不捏造
4. **投资类必加免责声明**："以上内容仅作信息整理与分析，不构成任何投资建议"
5. **六大违规不碰**：政治敏感/色情低俗/虚假谣言/商业欺诈/恶意诱导/侵权冒用
6. **克制冷调**：观察者视角，事实自证，冷自省比喻，禁甩锅受害者

## 反模式（写完必查）

| 反模式 | 修正方法 |
|--------|---------|
| 说教感（"你应该""记住"） | 改成观察者陈述，让事实自己说话 |
| AI味（问句标题/自问自答/列表堆砌） | 砍问号改陈述，用自然段落替代列表 |
| 无爆破句（全文没有一句想截图转发） | 必须有一句"打在心上"的判断 |
| 软收尾（"时间会给答案"） | 给读者一个具体判断，让转发者显得有见识 |
| 问句超密度（全文>5个问号） | 砍到3个以内，问完不能立刻自己答 |
| "你"密度过高（每段都以你开头） | 前两段出现"你"即可，后续用事实叙述 |
