# 网页视频演示模板

- 模板 ID：`tpl-garden-web-video-presentation`
- content-system templateId：`tpl-garden-web-video-presentation`
- 标签：工具 / 流程
- 来源 Skill：`web-video-presentation`
- 来源版本：`1.1.3`
- 来源链接：<https://github.com/ConardLi/garden-skills/tree/main/skills/web-video-presentation>
- 适合账号：`thinking-lab`、`visiontree`、`milo`、`eli`
- 内容类型：网页视频 / 动态演示 / 文章转口播录屏
- 适合素材：长文章、产品说明、技术拆解、认知模型、教程型素材、发布会式讲解素材
- title：网页视频演示模板
- format：16:9 点击驱动网页演示，可录屏成视频
- channels：B 站、YouTube、视频号、内部产品演示、创作者素材包
- Hook：用一个强反差判断或问题开场，让观众知道这不是普通 PPT，而是一段会逐步展开的解释视频。
- Structure：
  1. 识别输入：原始文章、已有口播稿或主题大纲。
  2. 先产出 `script.md` 和 `outline.md`，其中口播稿决定节拍，outline 只规划章节、步骤、信息密度和素材清单。
  3. 停在计划检查点，对齐稿子、outline、主题、素材准备方式和开发模式。
  4. 搭建 Vite + React + TypeScript 的 16:9 舞台，每次点击推进一个 `(chapter, step)`。
  5. 第 1 章必须先做成可验收的完整样板，作为本项目的视觉和代码锚点。
  6. 第 2 章以后按逐章确认、顺序开发或并行开发推进。
  7. 网页完成后再决定是否合成口播音频。
  8. 最后用手动点击或自动播放模式录屏，进入人工后期。
- Length：建议 3-8 分钟，4-8 章；每章 30-60 秒，每个 step 只承载一个想法。
- notes：
  - 适合账号：`thinking-lab` 用于认知模型图解和互动实验；`visiontree` 用于官方品类解释；`milo` 用于工程过程展示；`eli` 用于慢概念展开。
  - 适用素材：必须有足够原文细节或口播结构，不能只给一句空泛主题。
  - 兼容字段：可映射到 `title`、`format`、`channels`、`structure`、`hook`、`length`、`notes`、`resources`。
  - 使用方式：在创作者 brief 中引用本模板时，应附上原文、口播方向、推荐主题、需要准备的图片或数据素材。
  - 同步边界：这里只记录创作准备模板，不复制完整脚手架代码到 `content-system`。
- resources：
  - 来源资料：【Harness 实践：让 Agent 全自动制作知识讲解视频】<https://www.bilibili.com/video/BV1ypdgBCE9B/?share_source=copy_web&vd_source=c3f2a17dce62359215ab1773410de02b>
  - <https://github.com/ConardLi/garden-skills/tree/main/skills/web-video-presentation>
  - `skills/web-video-presentation/SKILL.md`
  - `skills/web-video-presentation/references/SCRIPT-STYLE.md`
  - `skills/web-video-presentation/references/OUTLINE-FORMAT.md`
  - `skills/web-video-presentation/references/CHAPTER-CRAFT.md`
  - `skills/web-video-presentation/references/AUDIO.md`
  - `skills/web-video-presentation/references/RECORDING.md`
- 使用边界：
  - 适合：有完整文章、口播稿、报告或产品说明，且内容需要逐步展开成视频化讲解。
  - 适合：有真实截图、产品画面、照片、图表或可生成的视觉素材，能让每个 step 有明确视觉锚点。
  - 慎用：只有一句主题、没有论证材料、案例或素材清单时，应先补资料。
  - 不适合：纯公告、纯口号、纯营销落地页，或需要复杂业务交互的应用页面。
- 运行效果：
  - 产物是 1920×1080 固定 16:9 网页舞台，点击、方向键或自动模式推进。
  - 观感应像为录屏设计的视频舞台，不像传统 PPT，也不应像营销页。
  - 典型项目包含 `script.md`、`outline.md`、`storyboard.md`、`style-guide.md`、素材清单、网页工程和验收截图。
  - 好结果的信号：每一步只表达一个想法，视觉锚点随口播节拍变化，第一章能独立作为风格样板。
- 使用方法：
  1. 先判断素材是否值得视频化：是否有清晰叙事、信息层次和视觉素材。
  2. 将原文改成自然口播稿，保留原文作为细节来源。
  3. 产出章节 outline，明确每章的 step、素材和信息密度。
  4. 先确认主题、视觉方向和第 1 章样板。
  5. 再开发完整 Vite + React + TypeScript 演示。
  6. 完成后用桌面和移动端截图验收，再决定是否合成音频或录屏。
- 最新案例：
  - `examples/labor-education-web-video/README.md`
  - 案例说明：把劳动教育结课报告做成 9 章点击驱动网页演示，包含口播稿、提词台本、章节规划、分镜、视觉风格、素材清单、网页工程和截图。
  - 截图：`examples/labor-education-web-video/screenshots/desktop-opening.png`、`mobile-opening.png`、`mobile-current.png`、`theory-scene.png`
- content-system 展示映射：
  - `title`：网页视频演示工具卡
  - `format`：网页视频 / 工具流程
  - `hook`：把文章、口播稿或产品说明变成可录屏的 16:9 点击驱动网页演示。
  - `structure`：判断素材 -> 准备输入 -> 拆口播节拍 -> 做第 1 章样板 -> 完整制作与录屏
  - `length`：3-8 分钟视频；4-8 章；每个 step 只承载一个想法。
  - `notes` 分组：适用范围、准备输入、使用边界、操作方式、运行效果、验收方式、最新案例、同步边界。
  - `resources` 重点：原始 Skill、来源视频、劳动教育网页视频案例和案例截图。
  - 前端展示目标：列表卡片帮助创作者判断“能不能套用”，详情页帮助创作者判断“怎么开始、会做成什么、哪里容易跑偏”。
- 语气：克制、清晰、有画面感；像认真做过分镜的产品 talk，不像模板化幻灯片。
- 禁忌：
  - 不把 VisionTree 写成已经成熟的“自动思考”产品。
  - 不把 Tree 写成已经落地的长期记忆或第二大脑能力。
  - 不把 outline 写成动画实现清单，动画应由章节实现时根据内容关系决定。
  - 不做纯文字翻页，每个 step 都应有明确视觉锚点。
  - 不虚构平台指标、用户结果或产品成熟度。
- 创作者提示：
  - 先判断素材是否值得做成视频。信息密度不够时，先补资料，不要直接套模板。
  - 第 1 章是风格样板，必须让人工创作者先看过再继续。
  - 口播稿和原文要同时保留：口播决定顺序，原文提供画面细节。
  - 推荐优先用于“解释一个复杂概念为什么重要”，而不是发布简单公告。
- 人工判断点：
  - 当前主题是否适合做视频，还是更适合短帖或图解。
  - 视频语气应偏教学、产品演示、还是观点陈述。
  - 哪些素材必须是真实截图 / 产品画面，哪些可以用 placeholder。
  - 是否需要合成音频，还是交给创作者真人录音。
- 同步到模板库：已同步
- 最近更新原因：2026-05-17 已根据 `C:\Users\Administrator\Documents\New project` 劳动教育结课报告网页视频案例补齐使用边界、运行效果、使用方法和最新案例截图；2026-05-11 已作为介绍卡片同步到 `content-system` 模板库。
