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
- 最近更新原因：2026-05-11 已作为介绍卡片同步到 `content-system` 模板库；保留完整工具说明在准备区，后续补真实案例截图。
